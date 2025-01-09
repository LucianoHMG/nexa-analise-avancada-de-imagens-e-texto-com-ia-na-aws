# Nexa - Análise Avançada de Imagens e Texto com IA na AWS

Este repositório apresenta um projeto prático utilizando **Amazon Textract**, um serviço da AWS especializado na extração de texto e dados estruturados de documentos digitalizados, como imagens e PDFs. O objetivo deste projeto é demonstrar como aplicar esse serviço, combinando outras ferramentas da AWS para análise avançada de imagens e textos.

## Objetivo

O projeto visa explorar as funcionalidades do **Amazon Textract** para:

- **Extração de texto**: Detectar e extrair texto de documentos, imagens e PDFs.
- **Reconhecimento de tabelas e formulários**: Identificar e extrair informações estruturadas, como tabelas e campos de formulários.
- **Automatização do fluxo de processamento de documentos**: Usar serviços da AWS para realizar o processamento em grande escala, de forma eficiente e automatizada.

## Tecnologias Utilizadas

- **Amazon Textract**: Para extração de texto, tabelas e formulários de documentos digitalizados (imagens e PDFs).
- **AWS Lambda**: Para automação do processamento sem a necessidade de gerenciar servidores.
- **Amazon S3**: Para armazenamento dos documentos de entrada e dos resultados da extração.
- **AWS CloudFormation**: Para provisionar e gerenciar a infraestrutura como código, criando e configurando recursos de forma automatizada.
- **Amazon Comprehend**: Para realizar análise de sentimentos e extração de entidades do texto extraído, complementando a análise de dados.

## Funcionalidades

1. **Extração de Texto e Dados Estruturados**
   - **Texto**: Extração de todo o conteúdo textual presente em imagens e PDFs.
   - **Tabelas e Formulários**: Identificação e extração de dados tabulares e campos de formulários, organizados em uma estrutura de fácil uso.

2. **Automação de Processamento com AWS Lambda**
   - Uso de funções Lambda para processamento automático dos documentos carregados no Amazon S3.

3. **Análise de Sentimentos e Entidades com Amazon Comprehend**
   - Análise do texto extraído para identificar sentimentos e entidades importantes, agregando valor ao processo de leitura de documentos.

## Pré-requisitos

Antes de executar o projeto, você precisará de:

- Uma conta AWS ativa com permissões para os serviços utilizados (Textract, Lambda, S3, etc.).
- AWS CLI configurado em seu ambiente local.
- Conhecimento básico sobre como utilizar GitHub e AWS.

## Como Executar

1. **Clone este repositório**  
   Para clonar o repositório no seu ambiente local, use o comando abaixo:  
   ```bash  
   git clone https://github.com/seu-usuario/nexa-analise-avancada  
   cd nexa-analise-avancada

2. Configure suas credenciais AWS
Configure as credenciais da AWS no seu terminal:

aws configure


3. Provisione os recursos com CloudFormation
Execute o comando abaixo para criar a infraestrutura necessária, incluindo buckets S3 e funções Lambda:

aws cloudformation deploy --template-file template.yaml --stack-name NexaAIProject


4. Envie seus Documentos para Análise

Carregue documentos (imagens ou PDFs) no bucket S3 configurado pela CloudFormation.

O Amazon Textract processará automaticamente esses documentos e extrairá o texto e dados estruturados.



5. Verifique os Resultados

Após o processamento, os resultados da extração estarão disponíveis no bucket S3 ou acessíveis via logs do Lambda.




Estrutura do Repositório

├── documents/             # Exemplos de documentos para análise
├── scripts/               # Scripts para interação com os serviços AWS
├── template.yaml          # Template de infraestrutura no CloudFormation
├── README.md              # Documentação do projeto

Licença

Este projeto está licenciado sob a Licença MIT.

Contribuições

Sinta-se à vontade para abrir issues ou enviar pull requests para melhorias e sugestões.


