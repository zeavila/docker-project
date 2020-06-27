# Docker-project

Estudo de Docker e Docker-Compose para aplicação Nodejs

# How To Run

Execute o commando `docker-compose up`.

# Docker on AWS

- Instale o AWS CLI: [veja aqui](https://docs.aws.amazon.com/pt_br/cli/latest/userguide/cli-chap-install.html)
- Configure o AWS CLI: rode o comando `aws configure`
- Instale o Docker-Machine: [Manual](https://docs.docker.com/machine/install-machine/)
- Crie um servidor EC2 na AWS: 
  - `docker-machine create --driver amazonec2 NodeAWS01`
  Onde "NodeAWS01" é o nome da sua instância a ser criada na AWS.
- Rode os comandos para utilizar a instância da AWS:
  - `docker-machine env NodeAWS01` - Onde "NodeAWS01" é o nome da instância criada.
  - `eval $(docker-machine env NodeAWS01)`
- Execute o comando `docker-compose up` para subir a sua aplicação na AWS.
- Configure o seu Security Group para liberar a porta da sua aplicação.
- Para voltar a utilizar comandos Docker na máquina local, execute o comando
  - `eval $(docker-machine env -u)`