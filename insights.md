# 💡 Insights e Aprendizados — AWS CloudFormation
## 🧠 Desafio: Implementando sua Primeira Stack com AWS CloudFormation
Este documento contém minhas anotações, reflexões e aprendizados obtidos durante o desafio da DIO, que teve como foco o uso do **AWS CloudFormation** para criar e gerenciar infraestrutura na nuvem de forma automatizada.

---
## 🏗️ 1. Conceitos Fundamentais

Durante o desafio, revisei os principais conceitos de **Infraestrutura como Código (IaC)** e como o **CloudFormation** se encaixa nesse contexto:
- **Infraestrutura como Código (IaC)**: permite definir toda a estrutura da nuvem (EC2, S3, IAM etc.) por meio de código, garantindo **padronização**, **agilidade** e **reprodutibilidade**.  
- **Stacks**: representam um conjunto de recursos criados e gerenciados em conjunto.  
- **Templates**: são arquivos YAML ou JSON que descrevem todos os recursos e suas propriedades.  
- **Parâmetros e Saídas (Parameters e Outputs)**: facilitam a personalização e reutilização dos templates em diferentes ambientes.

---
## ⚙️ 2. Etapas Realizadas
1. Criei um arquivo **YAML** contendo os recursos necessários para a Stack.  
2. Testei o template no **AWS CloudFormation Console** antes da implantação.  
3. Implantei a Stack e validei a criação dos recursos.  
4. Ajustei parâmetros e adicionei **Outputs** para exibir informações úteis.  
5. Capturei evidências (prints) e documentei todo o processo no GitHub.

---
## 🧩 3. Recursos Criados no Projeto

Durante o desafio, foram provisionados (ou simulados) os seguintes recursos AWS:
- **Amazon S3** — Bucket para armazenar dados e templates.  
- **Amazon EC2** — Instância simples para demonstrar o provisionamento automático.  
- **IAM Role** — Permissão para que a EC2 acesse o S3 (opcional).  
- **Outputs** — Mostrando nomes e IDs dos recursos criados.  

Esses recursos foram definidos de forma modular e reutilizável, seguindo boas práticas de IaC.

---
## 🔍 4. Principais Desafios e Soluções
| Desafio | Solução Aplicada |
|----------|------------------|
| Sintaxe YAML incorreta | Validei o template com o **AWS CloudFormation Linter** e o console da AWS. |
| Erros de permissão IAM | Ajustei a política da Role adicionando permissões mínimas necessárias. |
| Stack falhou durante criação | Analisei os logs de eventos no console e corrigi os parâmetros. |
| Nome de recursos duplicado | Utilizei variáveis e sufixos para gerar nomes únicos. |

---
## 💬 5. Aprendizados Pessoais
- Entendi melhor a importância de tratar **infraestrutura como código** para garantir consistência e escalabilidade.  
- Vi como o **CloudFormation** automatiza processos que levariam muito tempo se feitos manualmente.  
- Percebi o valor dos **parâmetros** e **outputs** para criar templates flexíveis e reutilizáveis.  
- Reforcei boas práticas de documentação técnica no GitHub, incluindo o uso de Markdown.

---
## 🚀 6. Próximos Passos

Como continuidade do aprendizado, pretendo:
- Criar templates mais complexos incluindo **VPCs, Subnets e Security Groups**.  
- Explorar o uso de **AWS SAM** e **CDK (Cloud Development Kit)** para abstrair templates CloudFormation em linguagens como Python ou TypeScript.  
- Integrar o **CloudFormation** a pipelines de **CI/CD (CodePipeline e CodeBuild)**.

---
## 🧾 7. Referências Utilizadas
- [Documentação Oficial — AWS CloudFormation](https://docs.aws.amazon.com/cloudformation/)
- [Guia de Boas Práticas AWS Well-Architected](https://aws.amazon.com/architecture/well-architected/)
- [Formação Code Girls | DIO](https://www.dio.me/)
- [Markdown Guide (GitHub)](https://www.markdownguide.org/)

---
## ✨ Autora
👩‍💻 **Bianca Gonçalves das Neves**  
📧 [biancagneves@gmail.com](mailto:biancagneves@gmail.com)  
💼 [linkedin.com/in/biancagneves](https://www.linkedin.com/in/biancagneves/)

---
> _“Infraestrutura como código não é apenas sobre automação — é sobre consistência, controle e confiança no seu ambiente.”_
