# Workflows Automatizados com AWS Step Functions



## ☁️ 1. O que é o AWS Step Functions

O AWS Step Functions é um serviço gerenciado da AWS que permite orquestrar múltiplos serviços da AWS em workflows visuais ou baseados em definições.


Você define estados que realizam tarefas, fazem escolhas, aguardam, etc., e o serviço cuida da execução, transição e monitoramento.



Ele é ideal para aplicações distribuídas, micro-serviços, pipelines de dados, automação de operações.

## 🧩 2. Principais Conceitos

- **Máquina de estados:** representa o workflow completo que você está orquestrando.


- **Estado:** cada passo dentro da máquina; pode ser do tipo Task, Choice, Wait, Pass, Parallel, Map, Succeed, Fail.

- **Realiza trabalho:** invoca uma função Lambda, chama uma API da AWS, etc.


## ⚙️ 3. Benefícios 

- Simplifica a orquestração de serviços — você não precisa construir “manual” cada integração.

- Visualização e monitoramento: histórico de execução, estados visuais, logs.

- Resiliência: suporte a retries, catch de erros, paralelismo, checkpointing, etc.

- Escalabilidade: adequado para alta carga, manipulação de muitos eventos, processamento em paralelo.


## 🛠️ 4. Boas Práticas

- Escolher corretamente o tipo de workflow: se for longa duração, precisa de auditoria, prefira Standard; se for alto volume, curta duração, prefira Express.

- Design de workflow modular: separe lógica de negócio das transições, mantenha estados simples e reutilizáveis.

- Observabilidade: ative logs e métricas no Amazon CloudWatch para acompanhar falhas, tempos, etc.



💡 Aprendizados do bootcamp

- Entender o fluxo de estados ajuda a desenhar sistemas que são robustos e menos propensos a erro humano.

- Adotar Step Functions nos tira do “código de orquestração” e coloca a gente no “foco da lógica de negócio”.

- Sempre que possível, visualizar o workflow no console do Step Functions ajuda a detectar gargalos ou loops desnecessários.

- O custo/execução importa: estados com muitos “loops” ou transições repetidas vão gerar custo — otimizar é tão importante quanto construir.


## 🧾 5. Referência e Leitura Recomendada

sformar processos compostos de múltiplas etapas em workflows visuais, automatizados, auditáveis e escaláveis. Saber estruturar as máquinas de estado, escolher o tipo correto (Standard vs Express), aplicar boas práticas de erro/tratamento/paralelismo e manter a observabilidade são os passos chave para dominar a orquestração de workflows na AWS.