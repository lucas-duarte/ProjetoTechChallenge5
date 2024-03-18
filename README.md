# ProjetoTechChallenge5

- Este é um projeto basico de uma API com .NET 8.0 para rodar em uma container
- Temos um arquivo Dockerfile, por onde foi gerado a imagem
- Um arquivo pod.yml dentro da pasta Yamls para gerar o pod

# Abaixo esta o passo a passo que realizei para rodar esse projeto:

- Dentro da pasta do projeto onde possui o DockerFile rodei o seguinte comando para criar a imagem:
  "docker build -t lucasduartep/techchallenge ."

- Realizei um push para da imagem para o Docker Hub:
   "docker push lucasduartep/techchallenge"

- Depois de logar no docker hub, rodei o comando "kubectl apply -f pod.yml" na pasta onde está o arquivo pod.yml para gerar a pod

- Posteriormente rodei o projeto no container rodando este comando: "kubectl port-forward projectapipod 7001:8080"
