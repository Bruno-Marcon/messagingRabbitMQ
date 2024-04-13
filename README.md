Relatório de Uso do RabbitMQ

Linguagem Utilizada: JavaScript (Node.js)

Introdução:
Neste relatório, descreveremos a implementação de produtores e consumidores de mensagens utilizando a linguagem JavaScript, com o ambiente Node.js, juntamente com a biblioteca amqplib para interagir com o RabbitMQ. A escolha dessa linguagem foi baseada na familiaridade com a mesma, e a praticidade na resolução de erros, embora a preparação do ambiente de desenvolvimento possa apresentar desafios.

Desafios:
A mair dificuldade no proceso foi a configuração do ambiente de desenvolvimento. Embora a linguagem JavaScript seja muito utilizada e o Node.js seja uma plataforma bem documentada, a configuração do ambiente para trabalhar com o RabbitMQ apresentou alguns problemas, principalmente em acertar a comunicação entre o client e o RabbitMQ. Alguns erros foram corrigidos alterando a forma de execução do RabbitMQ para o docker.

Implementação do Produtor:
O arquivo new_task.js é responsável por enviar mensagens para a fila do RabbitMQ. Utilizando a biblioteca amqplib, o código se conecta ao servidor RabbitMQ, declara a fila desejada (no caso, 'task_queue'), e envia a mensagem especificada ou uma mensagem padrão ('Hello World!'). Após o envio da mensagem, a conexão com o servidor é fechada.

Implementação do Consumidor:
O arquivo worker.js é responsável por consumir as mensagens da fila do RabbitMQ. Ele utiliza a biblioteca amqplib para se conectar ao servidor RabbitMQ e declarar a fila desejada ('task_queue'). Em seguida, ele aguarda mensagens na fila e, ao receber uma mensagem, processa.Após o processamento, a mensagem é confirmada para indicar ao RabbitMQ que foi processada com sucesso.

Conclusão:
A preparação do ambiente de desenvolvimento pode representar um estresse inicial. No entanto, uma vez configurado o ambiente, a comunicação com o RabbitMQ fica tranquilo o restante. É interessante como através de um exemplo simples é possivel ver a usabilidade em projetos maiores, relativamente tranquilo para desenvolver, porém muito focado na teoria, muito importante entender como cada processo deve funcionar.
