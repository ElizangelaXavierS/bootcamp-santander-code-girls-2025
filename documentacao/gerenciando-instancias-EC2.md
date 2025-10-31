# Gerenciamento de Instâncias EC2 (AWS)


## ☁️ 1. Conceito Geral

O Amazon EC2 (Elastic Compute Cloud) é o serviço da AWS que permite criar e gerenciar máquinas virtuais escaláveis na nuvem.
Essas instâncias funcionam como servidores virtuais que podem ser configurados conforme a necessidade do projeto.

### 📌 Principais características

- Escalável (pode aumentar ou reduzir capacidade conforme a demanda).

- Pagamento sob demanda.

- Totalmente personalizável (CPU, RAM, armazenamento, rede,etc).

- Alta disponibilidade (pode ser replicada em múltiplas zonas de disponibilidade).

## 🧩2. Componentes-Chave

| Componente         | Função                          |
| ------------------ | ------------------------------- |
| **AMI**            | Imagem base (SO e configs).     |
| **Instance Type**  | Define CPU, RAM, rede.          |
| **EBS**            | Armazenamento persistente.      |
| **Security Group** | Controle de tráfego (firewall). |
| **Elastic IP**     | IP público fixo.                |


## ⚙️ 3. Ciclo de Vida de uma Instância EC2

- **Inicialização:** Criação da instância com AMI, tipo e configuração definidos.
- **Em execução:**	Instância ativa, podendo ser acessada via SSH (Linux) ou RDP (Windows).
- **Parada:**	Instância desligada — não gera cobrança de compute, mas o EBS continua sendo cobrado.
- **Encerrada:**	Instância e dados são apagados permanentemente (se não houver snapshot).


## 🛠️ 4. Práticas de Gerenciamento 

✅ Boas práticas

- Sempre rotular instâncias com tags (Name, Environment, Owner).

- Criar snapshots regulares do volume EBS.

- Usar IAM Roles para controle de permissões em vez de chaves gravadas.

- Utilizar Auto Scaling Groups para gerenciar carga automaticamente.

- Implementar CloudWatch Alarms para monitoramento (CPU, status checks, etc).


💡 Aprendizados do bootcamp

- EC2 é a base de praticamente todos os serviços AWS — entender bem é essencial.

- O custo pode crescer rapidamente se não houver controle.

- Configurar corretamente Security Groups é fundamental para segurança e conectividade.


## 🧾 5. Referência e Leitura Recomendada

[Documentação Oficial — Amazon EC2 ](https://docs.aws.amazon.com/pt_br/toolkit-for-visual-studio/latest/user-guide/tkv-ec2-ami.html)

