# aws-dio-cod-girl-cloudformation-desafio-
🧠 Resumo do Desafio  Você vai:  Criar sua primeira Stack na AWS usando CloudFormation (ou seja, provisionar recursos com código YAML/JSON).  Documentar todo o processo técnico e seus aprendizados.  Organizar o material em um repositório GitHub público — que servirá como seu portfólio técnico.

# 🚀 Desafio DIO - AWS CloudFormation: Implementando sua Primeira Stack

Este repositório faz parte do desafio **"Implementando sua Primeira Stack com AWS CloudFormation"** da trilha **Code Girls | DIO**.  
O objetivo é aplicar, de forma prática, os conceitos de **Infraestrutura como Código (IaC)** utilizando o serviço **AWS CloudFormation**.

---

## 🧠 Objetivos de Aprendizagem

- Aplicar os conceitos aprendidos nas aulas práticas.  
- Criar, configurar e provisionar recursos AWS utilizando CloudFormation.  
- Entender o funcionamento de **templates YAML** e **parâmetros**.  
- Documentar processos técnicos de forma clara e organizada.  
- Utilizar o **GitHub** como ferramenta de versionamento e compartilhamento técnico.

---

## ⚙️ Tecnologias e Serviços Utilizados

- **AWS CloudFormation**  
- **Amazon S3** (para armazenar templates e objetos)  
- **Amazon EC2** (para criação de instâncias, se aplicável)  
- **IAM** (para permissões e papéis)  
- **GitHub / Markdown** (documentação e versionamento)  

---

## 🧩 Estrutura do Template

O template desenvolvido neste desafio realiza as seguintes tarefas:

1. Criação de um **bucket S3** para armazenamento de dados.  
2. Criação de uma **instância EC2** simples.  
3. Definição de **parâmetros, outputs e recursos**.  

📄 **Exemplo de Template (YAML):**

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: "Template de exemplo - Criação de um bucket S3 e uma instância EC2"

Parameters:
  InstanceType:
    Type: String
    Default: t2.micro
    Description: Tipo da instância EC2

Resources:
  S3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: meu-bucket-exemplo-cloudformation

  EC2Instance:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: !Ref InstanceType
      ImageId: ami-0c55b159cbfafe1f0 # Exemplo (Amazon Linux)
      Tags:
        - Key: Name
          Value: MinhaPrimeiraInstanciaCF

Outputs:
  BucketName:
    Description: Nome do bucket S3 criado
    Value: !Ref S3Bucket
  InstanceId:
    Description: ID da instância EC2 criada
    Value: !Ref EC2Instance
```
---

## 💡 Insights e Aprendizados

Durante o desafio, aprendi a:
1.Entender o funcionamento do CloudFormation e sua sintaxe YAML.
2.Criar recursos AWS automaticamente com segurança e rastreabilidade.
3.Reutilizar templates para diferentes ambientes (dev, test, prod).
4.Tratar erros de implantação e revisar logs de eventos da stack.
5.Valorizar o conceito de Infraestrutura como Código (IaC) na prática.
Mais detalhes no arquivo insights.md

---

## ✨ Autora

👩‍💻 Bianca Gonçalves das Neves
📧 biancagneves@gmail.com
💼 linkedin.com/in/biancagneves

---

## 🏁 Conclusão

Este desafio reforçou o poder da Infraestrutura como Código (IaC) através do AWS CloudFormation.
Com ele, é possível automatizar a criação de recursos na nuvem, reduzir erros manuais e manter um ambiente padronizado e escalável.
