# Identificação de Celebridades com AWS Rekognition

Este repositório demonstra o uso do serviço **AWS Rekognition** para identificar automaticamente celebridades em imagens. A aplicação aproveita a poderosa API de análise visual da AWS, permitindo reconhecimento facial e comparação com um banco de dados de celebridades.

## Funcionalidades

- **Reconhecimento de Celebridades**: Identifica celebridades em imagens carregadas para o S3 usando o AWS Rekognition.
- **Análise Facial**: Detecta faces nas imagens e mapeia com o banco de dados de celebridades da AWS.
- **Integração S3**: A aplicação processa imagens diretamente a partir de um bucket do S3.

## Pré-requisitos

Antes de começar, certifique-se de ter:

- Uma **conta AWS** com permissões para acessar o **Rekognition** e o **S3**.
- O **AWS CLI** instalado e configurado. Caso não tenha, instale com o comando:
  ```bash
  aws configure

Python 3.x instalado no seu sistema.


Como Executar

Siga os passos abaixo para configurar e rodar o projeto:

1. Clone este repositório

Clone o repositório para o seu ambiente local:

git clone https://github.com/seu-usuario/aws-rekognition-celebridades
cd aws-rekognition-celebridades

2. Instale as dependências

Instale os pacotes necessários para rodar o script:

pip install -r requirements.txt

3. Carregue uma imagem no Amazon S3

Faça o upload da sua imagem para um bucket do Amazon S3. Para isso, crie um bucket no S3 e envie suas imagens manualmente ou use o seguinte comando para fazer o upload via CLI:

aws s3 cp /caminho/para/sua/imagem.jpg s3://seu-bucket/nome-da-imagem.jpg

4. Configure suas credenciais AWS

Certifique-se de que o AWS CLI está configurado corretamente:

aws configure

5. Execute o Script

Agora, execute o script identify_celebrity.py passando a URL da imagem no S3 como parâmetro:

python identify_celebrity.py --image s3://seu-bucket/nome-da-imagem.jpg

6. Verifique os Resultados

O script irá processar a imagem e retornar uma lista de celebridades identificadas, com as informações detalhadas sobre as faces detectadas.

Licença

Este projeto está licenciado sob a Licença MIT.

Contribuições

Contribuições são bem-vindas! Se você encontrar um bug ou tiver uma melhoria para sugerir, abra uma issue ou envie um pull request.


---

Sobre o Projeto

Este repositório faz parte do curso "Análise de Imagens e Texto com IA na AWS", oferecido pela Digital Innovation One. Durante o curso, aprendi a usar diversos serviços da AWS, com foco no AWS Rekognition, para realizar tarefas de análise visual, como a identificação de celebridades em imagens. Aproveite este código como base para suas próprias aplicações de análise de imagens!

Este arquivo contém todos os passos necessários para configurar, executar e entender o funcionamento do projeto com o **AWS Rekognition**. Não esqueça de substituir `LucianoHMG` e o caminho do S3 pelo valor correto no seu projeto!

