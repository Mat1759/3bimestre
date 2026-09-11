# Introdução ao RabbitMQ

> RabbitMQ é um sistema de mensageri no qual o produtor publica uma mensagem, a exchange recebe a mensagem e decide para quais filas ela será encaminhada.
>
> As filas mantém as mensagens até que s consumidores possam processá-las. Essa organização separa quem envia, como a mensagem é roteada e quem consome. O resultado é um sistema mais flexível e desacoplado, pois o produtor não precisa conhecer diretamente a fila ou o consumidor.