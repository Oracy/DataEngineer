# EDA Event Driver Architecture

A **Arquitetura Orientada a Eventos (Event-Driven Architecture - EDA)** é um estilo de arquitetura onde as ações e interações entre componentes do sistema são disparadas por eventos, que podem representar qualquer mudança significativa no estado de um sistema, como uma transação realizada, uma mensagem recebida ou uma atualização de dados.

### Principais conceitos da EDA:

1. **Evento**: Representa uma ocorrência significativa no sistema, como "novo pedido", "usuário cadastrado" ou "pagamento realizado". Cada evento é uma mensagem que carrega informações sobre a ação ou mudança que ocorreu.

2. **Produtor de eventos**: Um componente que gera eventos. Pode ser uma aplicação, um serviço ou qualquer sistema que observe uma mudança de estado e dispare um evento.

3. **Consumidor de eventos**: Um componente que escuta eventos e age de acordo com eles. Pode ser um serviço, uma aplicação ou um pipeline de processamento que realiza ações com base no evento recebido.

4. **Broker (Intermediário de mensagens)**: Um sistema que recebe eventos dos produtores e os distribui para os consumidores. Exemplos comuns incluem Apache Kafka, RabbitMQ e AWS Kinesis.

5. **Stream de Eventos**: É uma sequência contínua e em tempo real de eventos que são emitidos por um ou mais produtores e consumidos por um ou mais consumidores. Os eventos fluem continuamente por um canal, como um stream de dados.

### Utilização de Streams de Eventos em EDA:

Streams de eventos são usados para processar dados em tempo real, o que permite que sistemas reajam instantaneamente a eventos. Em vez de esperar por um processamento em batch, o sistema pode responder assim que um evento ocorre, oferecendo maior agilidade e escalabilidade.

#### Exemplos de utilização:
- **Monitoramento de dados em tempo real**: Empresas podem monitorar transações financeiras, dados de sensores ou métricas de sistema em tempo real, gerando alertas instantâneos ou ajustando estratégias de acordo com mudanças.
  
- **Processamento contínuo de dados**: Ferramentas como Apache Kafka Streams ou Apache Flink permitem aplicar operações complexas sobre streams de eventos, como agregações, filtragens e transformações.

- **Microservices e comunicação assíncrona**: Em um ambiente de microsserviços, eventos são usados para permitir que serviços se comuniquem de forma assíncrona. Um serviço pode emitir um evento quando uma ação é concluída (como "pedido concluído"), e outros serviços que precisam saber disso podem consumir esse evento e agir de acordo.

### Principais vantagens de EDA com streams de eventos:
1. **Desacoplamento**: Produtores e consumidores de eventos podem operar independentemente uns dos outros. Isso facilita a escalabilidade e manutenção do sistema.
2. **Escalabilidade**: Como os consumidores processam eventos de forma assíncrona e independente, a arquitetura permite fácil escalabilidade horizontal.
3. **Resiliência**: Caso algum consumidor ou parte do sistema falhe, o sistema pode ser projetado para reprocessar eventos ou continuar a funcionar sem afetar o sistema como um todo.
4. **Baixa latência**: Processamento em tempo real permite respostas rápidas a eventos críticos.

### Ferramentas comuns para implementar EDA com streams de eventos:
- **Apache Kafka**: Um dos sistemas de mensagens e streaming mais utilizados para implementar pipelines de eventos. Kafka armazena streams de eventos de forma durável e permite escalabilidade em grandes volumes de dados.
- **AWS Kinesis**: Serviço gerenciado da Amazon para streaming de dados em tempo real.
- **Apache Pulsar**: Uma alternativa ao Kafka com mais foco em latência ultrabaixa e suporte nativo para georreplicação.

Esse tipo de arquitetura é fundamental em sistemas que exigem alta performance, escalabilidade e processamento em tempo real, como no caso de sistemas financeiros, IoT, e-commerce e redes sociais.