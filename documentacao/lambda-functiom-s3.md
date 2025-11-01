# Tarefas Automatizadas com AWS Lambda e S3


## ☁️ 1. Conceito Geral

A combinação entre AWS Lambda e Amazon S3 é uma das formas mais eficientes de automatizar tarefas na nuvem sem precisar de servidores.

Lambda: executa código sob demanda (serverless).

S3 (Simple Storage Service): armazena e gerencia objetos (arquivos).

Juntos, permitem disparar funções automáticas ao ocorrer eventos, como upload, exclusão ou atualização de arquivos.

Com Lambda + S3, o código só roda quando algo acontece — e você só paga pelo tempo de execução.

## 🧩 2. Funcionamento da Automação
🔁 Fluxo Básico

- Um evento ocorre no S3 (ex: upload de arquivo).

- O evento dispara uma função Lambda automaticamente.

- A função processa o arquivo (ex: redimensiona imagem, gera log, extrai metadados, etc).

- (Opcional) O resultado é salvo de volta no S3 ou enviado para outro serviço (DynamoDB, SNS, SQS...).





## ⚙️3. Casos de Uso Comuns

| Cenário                            | Descrição                                                      |
|------------------------------------| -------------------------------------------------------------- |
| **Processamento de imagens**       | Geração de miniaturas, compressão ou metadados.                |
| **Automação de logs**              | Movimentação, renomeação ou arquivamento automático.           |
| **Integração com bancos de dados** | Atualizar tabelas no DynamoDB após upload.                     |
| **Pipelines de dados**             | Converter formatos (ex: CSV → JSON) automaticamente.           |
| **Machine Learning**               | Disparar inferência automática após upload de imagem ou áudio. |

## 🛠️ 4.Boas Práticas

**Segurança**

- Crie uma IAM Role específica com permissões mínimas (principle of least privilege).


 **Escalabilidade**

- Use Lambda Layers para dependências externas.

- Aumente o timeout e a memória conforme o tipo de processamento.

**Logs e Monitoramento**

- Habilite Amazon CloudWatch Logs para acompanhar execuções e erros.
- Crie Alarmes para falhas recorrentes.

**Eficiência**

- Prefira processamentos curtos (máx. 15 min).

- Para fluxos mais longos → use Step Functions para orquestrar.


💡Aprendizados do Bootcamp

- Automatizar tarefas com Lambda + S3 elimina processos manuais repetitivos.

- O modelo event-driven (baseado em eventos) torna o sistema altamente escalável.

- Integrar com CloudWatch é essencial para entender falhas e otimizar custo.

- Quanto mais modular o código Lambda, mais reutilizável ele se torna.

- A segurança (via IAM e política de buckets) deve ser pensada desde o início.

- Lambda é ponto de entrada para arquitetura serverless — dominar esse conceito é chave para avançar na nuvem AWS.

## 🧾 5. Referência e Leitura Recomendada


[Documentação AWS - Automatizar a configuração do S3 Object Lambda com um modelo do CloudFormation ](https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/olap-using-cfn-template.html)