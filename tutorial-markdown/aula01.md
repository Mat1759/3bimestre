# *Introdução*
    O Markdown é uma linguagem de marcação simples para formatar textos de maneira rápida e legível no GitHub e completamente usada para:

    - arquivos "README.md"
    - documentação de projetos
    - anotações técnicas
    - relatórioss de atividades
    - instruçõs de instalações
    - registros de aulas
    - issues e pull requests

    A extensão padrão do arquivo markdown é ".md"

    Exemplo:
        README.md
    
## 1. O que é o $Markdown$?
    Markdown permite aplicar formatação simples em um texto usando caracteres simples;

Exemplo:
           
### Meu projeto 

Este projeto foi desenvolvido durante a aula de **Versionamento de código**

#### Tecnologias
- Git
- GitHub
- VSCode

No GitHub, esse conteúdo será apresentado de forma formatada com título, texto em negrito e listagem.

## 2. $Criando$ um arquivo Markdown.

No Visual Code Studio:

1. Abra a pasta do Projeto
2. Clique em ***"new file"***
3. Informe o nome do arquivo

Ex: *README*.md

Para registros de aulas, também podem ser utilizadas nomes como;

        semana-01.md
        semana-02.md
        aula-01.md

# Boas Práticas
> $Prefiranomes$:
    
- curtos;
- descritos;
- escrito em letras minúsculas;
- sem acentos;
- sem espaços;
- separados por hífen quando necessário.

---

> $Recomendado$

- resumo-git.md
- aula-01.md
- comandos-git.md

---

> $Evite$

- Resumo Git.md
- Aula 01.md
- Atividade Prática GitHub.md
- Meu Arquivo Novo.md

---

# 3. Título e subtítulos
Markdown utiliza a caractere # para criar títulos

```markdown
# Título Principal
## Título nível 2
### Título nível 3
#### Título nível 4
##### Título nível 5
###### Título nível 6
```

# Título Principal
## Título nível 2
### Título nível 3
#### Título nível 4
##### Título nível 5
###### Título nível 6

## Boa Prática
> Utilize uma estrutura hierárquica

- Exemplo:

# Semana 08 - Introdução ao Git
## Objetivos da aula
## Conceitos aprendidos
### Repositório
---
### Commit
---
### Branch
---
### Atividade Prática
---
## Conclusão

Evite pular níveis sem necessidade:

# Título
### Subtítulo

---
# 4. Parágrafos
    
  Para criar um parágrafo, deixe uma linha em branco entre os textos.
    
    Git é um sistema de controle distribuído

    Ele permite registrar e acompanhar alterações realizadas nos arquivos de um projeto.

# 5. Negrito

Utilize 2 asteriscos:
```markdown
**texto em negrito**
```
O **Git** é um sistema de controle de versão

# 6. Itálico
Utilize 1 asterisco:
```markdown
*texto em itálico*
```
O comando *git status* permite verificar o estado do repositório.

Entretanto para representar comandos, o ideal é utilizar a formatação de código a seguir.

# 7. Negrito e Itálico
```markdown
 ***texto em negrito e itálico***
 ```
> ***git add***

# 8. Listas não ordenadas
Utilize antes de cada item.
```markdown
- Git
- GitHub
- Visual Code Studio
```

Também é possível criar níveis
```markdown
- Git
  - Commit
  - Branch
  - Merge
  ```
- GitHub
  - Repositório
  - Pull Request
  - Issues

Utilize listas para representar
- Conceitos
- Requisitos
- Tecnologias
- Etapas
- Recursos

# 9. Listas Numeradas
```markdown
1. Criar o repositório
2. Adicionar os arquivos
```
3. Criar o commit
4. Enviar para o GitHub

Ideal para procedimentos que precisam ser executados em ordem.

# 10. Listas de Tarefas - CheckLists

O GitHub permite criar caixas de seleção
```markdown
- [x] Criar o repositório
- [ ] Criar o README
```
- [x] Realiza a atividade
- [ ] Criar o commit
- [x] Enviar para o GitHub

Esse recurso é especialmente útil para acompanhar atividades e projetos.