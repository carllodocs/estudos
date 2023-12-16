# Learning Plan of Cloud Essentials - Knowledge Badge Readiness Path

Este curso disponibilizado pela **Amazon Web Services training and certification** promete introduzir os principais conceitos relacionados à computação em nuvem, estando dividido por vários sub-cursos.

## 1º curso: Job Roles in The Cloud

Nessa seção, foi retratado, como aspecto-chave, a transição de uma equipe empresarial que segue o modelo **On-Premises** (relativo a servidores locais) para o **Shared Responsability Model** (referente à relação com o provedor de nuvem), no qual a Amazon estaria responsável pelas tarefas e segurança "da" nuvem, e o cliente, pelas funções e seguridades "na" nuvem.

Sendo assim, uma equipe tradicional do primeiro modelo teria a divisão dos seguintes cargos:

- IT Solutions Architect
- System Administrator
- Network Administrator
- Desktop Administrator
- Applications Administrator
- Database Administrator

Enquanto a nova equipe contaria com as seguintes funções:

- Cloud Architect
- System Administrator
- Security Administrator
- DevOps Administrator

## 2° curso: AWS Cloud Practitioner Essentials

### Módulo 1: Introduction to Amazon Web Services

Aqui foram apresentados os três modelos com os quais se pode trabalhar utilizando os serviços de computação em nuvem da Amazon, sendo eles:

- Cloud
- Hybrid
- On-Premises (Private Cloud Deployment)

Ao se utilizar serviços como o **Amazon EC2** (Amazon Elastic Compute Cloud), por exemplo, segue-se um modelo escalável conhecido como **pay-as-you-go**, que permite ter despesas variáveis sem a preocupação com excessos ou limitações da capacidade do servidor. Com isso, é possível distribuir os sistemas com baixa latência, para diversos consumidores localizados ao redor do mundo.

Artigos recomendáveis que sintetizam tais ideias são:

- [Getting Started with AWS Cloud Essentials](https://aws.amazon.com/getting-started/cloud-essentials)
- [Types of Cloud Computing](https://aws.amazon.com/types-of-cloud-computing)

### Módulo 2: Compute in The Cloud

**Compute as a Service (CaaS)**: Modelo utilizado pelas instâncias de Amazon EC2 sob a ideia de **multitenancy**, em que hardwares de máquinas virtuais são compartilhados de uma maneira verticalmente escalável e segura. São três as etapas para seu funcionamento:

- Launch
- Connect
- Use

Sendo assim, há vários tipos de instância da Amazon EC2, como:

- **General purpose instances**, para um balanço de recursos
- **Compute optimized instances**, para processadores de alta performance
- **Memory optimized instances**, para o carregamento de dados em alta performance na CPU
- **Accelerated computing instances**, para uma agilização no processamento de dados
- **Storage optimized instances**, para armazenagem de dados com alto nível de IOPS

Dessa forma, há várias possibilidades de custeamento para essas instâncias, sendo elas:

- **On-Demand**, para trabalhos imprevisíveis a curto-prazo
- **Standard Reserved Instances**, para a especificação da família, tamanho, plataforma, locação e região em período de 1 ou 3 anos
- **Convertible Reserved Instances**, para mais descontos ao se flexibilizar a zona de disponibilidade da instância, em contrato de 1 ou 3 anos
- **EC2 Instance Saving Plans**, para a assumida de um comprometimento de gasto por hora em uma família, por 1 ou 3 anos
- **Spot Instances**, para realização de tarefas passíveis de interrupção de acordo com as capacidades disponíveis no momento
- **Dedicated Hosts**, para o licenciamento de uma reserva de socket, core ou máquina virtual

O manejo dessas instâncias pode ser feito com a utilização do **Amazon EC2 Auto Scaling**, que automaticamente adiciona ou encerra instâncias de Amazon EC2 conforme as variações de demanda, dentro de um espectro mínimo, desejado e máximo (**Auto scaling group**), reduzindo-se as despesas. Isso pode ocorrer de duas maneiras:

- Dynamic scaling
- Predictive scaling

**Elastic Load Balancing**: Serviço da AWS que, partindo de um único ponto de host, distribui automaticamente o tráfico para os recursos de back-end mais adequados, a nível regional, e aumentando ou diminuindo sua capacidade conforme aos diferentes períodos de demanda. Isso evita sobrecargas em uma única instância.

Nesse contexto, cabe a diferenciação entre os chamados **tightly coupled components** e os **loosely coupled components**, os quais, respectivamente, referem-se a **aplicações monolíticas** e aos **microsserviços** — esta última abordagem sendo mais eficiente para prevenir que todo o sistema falhe, a partir de erros em um dos componentes. Assim, o envio de mensagens de um componente para outro pode ser feito por intermédio de uma **Message Queue**, como o **SQS** e o **SNS**.

**Amazon Simple Queue Service (SQS)**: Serviço independente de fila que permite o envio, o armazenamento e a recepção de mensagens (payloads) entre componentes de um software a qualquer volume e de forma escalável, até que sejam processadas.

**Amazon Simple Notification Service (SNS)**: Serviço que pode enviar mensagens e notificações a partir do modelo **publish/subscribe**, a partir de um canal de um tópico, o qual distribui tais atualizações para todos os inscritos (como servidores web, endereços de email e funções Lambda da AWS) em determinado canal.

Outros serviços computacionais oferecidos pela Amazon, referentes ao conceito de **serverless computing** (em que o código roda em servidores que não precisam de ser provisionados ou administrados), são a AWS Lambda e a orquestração de Containers.

**AWS Lambda**: Serviço de serverless computing em que um código enviado roda apenas a partir de um evento acionado, sendo custeado o tempo de computação usado, sendo esse período menor que 15 minutos.

**Amazon Elastic Container Service (Amazon ECS)**: Sistema escalável de administração de containers Docker (open-source e empresarial).

**Amazon Elastic Kubernetes Service (Amazon EKS)**: Sistema escalável de administração de containers Kubernetes.

**AWS Fargate**: Mecanismo de computação para o Amazon ECS e EKS que administra a infraestrutura do servidor.

Há um resumo sobre esses tópicos disponível em:

- [Compute on AWS](https://aws.amazon.com/products/compute)