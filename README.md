# apachekafka_helloworld

### Download
```
- Faça o download do Apache Kafka 
  -https://kafka.apache.org/downloads
- Selecione a versão 0.10.2.1 e Scala 2.12
```

### Extração
```
- Extraia a pasta raiz do disco local C
  -Isso facilitará a execução dos comandos
```

### Execução
```
- Abra 3 cmds, caminhe até a pasta gerada pela extração do Kafka e execute os seguintes comandos respectivamente:
  C:\kafka_2.12-0.10.2.1>.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
    Esse comando irá startar o Zookeeper
  
  C:\kafka_2.12-0.10.2.1>.\bin\windows\kafka-server-start.bat .\config\server.properties
    Esse comando irá startar o Apache Kafka
    Antes de executar a 3° linha de comando, dê um "run" no SpringBootHelloWorldApplication.java
   
    
  C:\kafka_2.12-0.10.2.1>.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic java_in_use_topic --from-beginning
    Esse comando, fará com que o Consumer se inscreva no tópico e passe a receber mensagens de produtores
    
```

### Envie mensagem para o Consumer
```
- Abra um navegador e cole esta url
  http://localhost:8080//javainuse-kafka/producer?message=Hello World
  após o "...message=" será a mensagem criada pelo produtor
  Que neste exemplo está sendo "Hello World"
```


