# Implementando uma Infraestrutura Automatizada com AWS CloudFormation


## ☁️ 1. Visão Geral
O AWS CloudFormation é o serviço da AWS que permite criar, atualizar e gerenciar infraestrutura de forma automatizada usando templates declarativos (YAML ou JSON).
Com ele, é possível provisionar redes, instâncias, bancos de dados, funções Lambda, S3, IAM, entre outros recursos — tudo versionado e reproduzível.

## 🧩 2. Por que Automatizar a Infraestrutura

| Benefício                | Descrição                                                    |
| ------------------------ | ------------------------------------------------------------ |
| **Padronização**         | Mesma configuração em todos os ambientes (dev, stage, prod). |
| **Reprodutibilidade**    | Fácil recriar ambientes com o mesmo template.                |
| **Escalabilidade**       | Ajustes e expansões rápidas via código.                      |
| **Auditoria**            | Controle de versão, histórico e rastreabilidade.             |
| **Integração com CI/CD** | Deploy automatizado de recursos via pipelines.               |


## ⚙️  3. Estrutura básica de um Template
Um template define a infraestrutura completa da aplicação.

```
AWSTemplateFormatVersion: "2010-09-09"
Description: "Infraestrutura automatizada com CloudFormation"

Parameters:
EnvType:
Type: String
Default: dev
AllowedValues: [dev, prod]

Resources:
AppBucket:
Type: AWS::S3::Bucket
Properties:
BucketName: !Sub "app-${EnvType}-bucket"

Outputs:
BucketName:
Description: "Nome do bucket criado"
Value: !Ref AppBucket

```

Partes principais:


- **Parameters:** permite customizar a stack.
- **Resources:** define o que será criado.
- **Outputs:** exporta dados úteis após a criação.
- **!Sub e !Ref:** funções internas para interpolação e referência.


## 🛠️ 4.Boas Práticas

**Infraestrutura Modular**
- Separe recursos por propósito: rede, aplicação, dados.
- Use Nested Stacks para manter o template organizado.


**Controle de Versão**
- Armazene templates no Git.
- Use versionamento semântico (v1, v2, etc).


**Segurança** 
- Nunca defina credenciais fixas em templates.
- Use IAM Roles com permissões mínimas.

💡Aprendizados do Bootcamp

- Criar infraestrutura manual é rápido no início, mas não escala.
- CloudFormation permite reproduzir ambientes complexos com um único comando.
- A validação de template é essencial antes de cada deploy.
- O rollback automático é uma das maiores vantagens em ambientes críticos.
- Infraestrutura como código não é só técnica — é cultura de automação e consistência.


## 🧾 5. Referência e Leitura Recomendada


[Documentação AWS - CloudFormation](https://docs.aws.amazon.com/pt_br/AWSCloudFormation/latest/UserGuide/Welcome.html)