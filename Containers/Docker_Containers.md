# Docker e Container

Docker é uma plataforma de código aberto que permite criar, distribuir e rodar aplicações em **containers**. Containers são pacotes que incluem a aplicação e todas as suas dependências, como bibliotecas, configurações e até o sistema operacional, garantindo que a aplicação rode de forma consistente em diferentes ambientes.

### Principais conceitos:
1. **Imagem**: Um arquivo imutável que contém tudo o que é necessário para executar uma aplicação, como código, dependências, e ferramentas. Imagens são como "moldes" usados para criar containers.
   
2. **Container**: Uma instância em execução de uma imagem. Um container isola o ambiente da aplicação, garantindo que ela funcione de maneira consistente independentemente da máquina ou do sistema operacional.

3. **Dockerfile**: Um script de texto que define passo a passo como construir uma imagem Docker, incluindo comandos de instalação de dependências e cópia de arquivos.

4. **Registro de Imagens (Docker Hub)**: Um repositório onde as imagens podem ser armazenadas e compartilhadas. O Docker Hub é o registro público mais popular, mas você pode criar registros privados.

### Vantagens de usar Docker:
- **Portabilidade**: Os containers podem ser executados em qualquer lugar, desde que o host tenha o Docker instalado, o que elimina problemas como "funciona na minha máquina, mas não no servidor".
- **Isolamento**: Cada container tem seu próprio ambiente, o que evita conflitos de dependências entre diferentes projetos ou versões de uma aplicação.
- **Eficiência**: Docker usa menos recursos que máquinas virtuais, já que os containers compartilham o kernel do host, o que resulta em mais performance e menor uso de recursos.

### Comandos básicos:
- `docker build`: Cria uma imagem a partir de um Dockerfile.
- `docker run`: Executa um container a partir de uma imagem.
- `docker ps`: Lista os containers em execução.
- `docker stop`: Para um container.
- `docker pull`: Baixa uma imagem do Docker Hub.
