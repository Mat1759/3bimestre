import pandas as pd
import numpy as np
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA

# semente aleatória
np.random.seed(42)

# tabela dados com valores aleatórios
dados = pd.DataFrame({
    "horas_estudo": np.random.randint(1, 6, 50),
    "exercicios": np.random.randint(10, 100, 50),
    "frequencia": np.random.randint(60, 100, 50),
    "participacao": np.random.randint(1, 10, 50),
})

dados["nota_anterior"] = (
    dados["horas_estudo"] * 1.5
    + np.random.normal(0, 1, 50)
)

print("\n--- Primeiras linhas da base ---")
print(dados.head())

correlacao = dados.corr()

print("\n--- Matriz de correlação ---")
print(correlacao.round(3))

dados_selecionados = dados.drop(columns=["nota_anterior"])

print("\n--- Dados após retirar nota_anterior ---")
print(dados_selecionados.head())

scaler_engajamento = StandardScaler()

engajamento_padronizado = scaler_engajamento.fit_transform(
    dados[["frequencia", "participacao"]]
)

dados["engajamento_total"] = (
    engajamento_padronizado[:, 0]
    + engajamento_padronizado[:, 1]
)

print("\n--- Nova feature: engajamento_total ---")
print(
    dados[
        ["frequencia", "participacao", "engajamento_total"]
    ].head()
)

features_pca = [
    "horas_estudo",
    "exercicios",
    "frequencia",
    "participacao"
]

X = dados[features_pca]

scaler = StandardScaler()
X_padronizado = scaler.fit_transform(X)

pca = PCA(n_components=2)
componentes = pca.fit_transform(X_padronizado)

dados_pca = pd.DataFrame(
    componentes,
    columns=["Componente_1", "Componente_2"]
)

print("\n--- Dados após PCA ---")
print(dados_pca.head())

print("\n--- Variância explicada ---")

print(
    "Componente 1:",
    round(pca.explained_variance_ratio_[0] * 100, 2),
    "%"
)

print(
    "Componente 2:",
    round(pca.explained_variance_ratio_[1] * 100, 2),
    "%"
)

print(
    "Total explicado pelos dois componentes:",
    round(
        pca.explained_variance_ratio_.sum() * 100,
        2
    ),
    "%"
)
