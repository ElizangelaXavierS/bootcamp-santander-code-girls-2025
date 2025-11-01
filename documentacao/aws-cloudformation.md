# Primeira Stack com AWS CloudFormation


## ☁️ 1. O que é o AWS CloudFormation

O AWS CloudFormation é um serviço que permite provisionar e gerenciar infraestrutura AWS via código.
Em vez de criar recursos manualmente no console, descrevemos tudo (instâncias, VPCs, S3, IAM, etc.) em um template YAML ou JSON.


## 🧩 2. Conceitos-Chave

- **Stack:**	Conjunto de recursos criados e gerenciados juntos a partir de um template.
- **Template:**	Arquivo YAML/JSON que define os recursos AWS.
- **Resources:**	Itens criados (ex: S3 bucket, EC2, Lambda).
- **Parameters:**	Valores dinâmicos definidos pelo usuário ao criar a stack.
- **Outputs:**	Informações retornadas após a criação (ex: URL, ARN, IP).
- **Change Set** 	Visualização de alterações antes de atualizar a stack.

## ⚙️ 3. Criando a Primeira Stack 
🖥️ Via Console

- Acesse AWS CloudFormation → Create Stack → With new resources (standard).

- Faça o upload do seu arquivo .yaml ou .json.

- Dê um nome à stack.

- (Opcional) Defina parâmetros, tags e permissões.

- Clique em Create stack.

- Acompanhe o status de criação em tempo real.





## 🛠️ 4.Boas Práticas

- Versione seus templates no Git (cada stack = uma release).

- Sempre valide o template antes de criar:

- Use Parameters para tornar o template reutilizável.

- Utilize Outputs para facilitar integrações entre stacks.


💡 Aprendizado do Bootcamp

- Automatizar = reduzir erro humano.

- CloudFormation ensina pensar em infraestrutura como software.

- Se algo falhar, CloudFormation faz rollback automático.

- Entender a hierarquia (Stack, Resources, Parameters) é essencial antes de avançar para arquiteturas complexas.


## 🧾 5. Referência e Leitura Recomendada


[Documentação AWS - CloudFormation](https://docs.aws.amazon.com/pt_br/AWSCloudFormation/latest/UserGuide/Welcome.html)