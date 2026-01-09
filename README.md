# 📧 Email Service

API REST para envio de e-mails utilizando Java, Spring Boot e AWS SES, desenvolvida como desafio backend.

---

## 📌 Visão Geral

Este projeto consiste em um microserviço backend responsável pelo envio de e-mails a partir de uma API REST.
Ele foi desenvolvido seguindo as diretrizes de um desafio técnico backend, com foco em organização, boas práticas, abstração de serviços externos e preparo para ambiente de produção.

A aplicação realiza a integração com o AWS Simple Email Service (SES) para envio de mensagens.

---

## 🧠 Contexto do Desafio

**Desafio escolhido:** Email Service

**Objetivo funcional:**  
Criar um serviço que receba informações de e-mail e realize o envio por meio de um provedor externo, abstraindo essa dependência para permitir futuras substituições ou estratégias de failover sem impacto para os clientes do serviço.

**Trilha técnica:**  
Back-end — API REST pensada para ser consumida por outros sistemas.

---

## 🚀 Funcionalidades Implementadas

- API REST para envio de e-mails
- Integração com AWS Simple Email Service (SES)
- Abstração do provedor de e-mail através de interface
- Implementação concreta do provedor AWS SES
- Tratamento de exceções e erros de envio
- Estrutura organizada com separação de responsabilidades
- Endpoint pronto para testes via Postman

---

## 🛠️ Tecnologias Utilizadas

- Java 21  
- Spring Boot  
- Spring Web  
- AWS Simple Email Service (SES)  
- AWS SDK for Java  
- Maven  
- Postman  

---

## 📚 Aprendizados

Durante o desenvolvimento deste projeto, foram praticados e consolidados os seguintes conceitos:

- Integração de aplicações Java com serviços da AWS
- Configuração e utilização do AWS SDK
- Criação de APIs REST com Spring Boot
- Uso de abstrações para desacoplamento de serviços externos
- Tratamento adequado de exceções e respostas HTTP
- Diagnóstico e resolução de erros comuns em backend (erro 500, credenciais AWS, conexão)
- Estruturação de um projeto backend com foco em produção

---

## ⚙️ Instalação e Configuração

### Clonar o repositório
```bash
git clone https://github.com/seu-usuario/email-service.git
Configurar credenciais da AWS
No arquivo application.properties (ou via variáveis de ambiente):

properties
Copiar código
aws.region=us-east-1
aws.accessKeyId=SUA_ACCESS_KEY
aws.secretKey=SUA_SECRET_KEY
⚠️ Caso sua conta AWS esteja em modo Sandbox do SES, os e-mails de remetente e destinatário precisam estar verificados no console da AWS.

▶️ Executando a Aplicação
Execute o projeto com Maven:

bash
Copiar código
mvn spring-boot:run
A API estará disponível em:

arduino
Copiar código
http://localhost:8080
📡 Endpoints da API
Enviar E-mail
POST /api/email/send

Corpo da requisição
json
Copiar código
{
  "to": "exemplo@email.com",
  "subject": "Teste de envio",
  "body": "Este é um e-mail enviado via AWS SES"
}
Respostas possíveis
200 OK — E-mail enviado com sucesso

500 Internal Server Error — Erro ao enviar o e-mail

🧩 Observações de Arquitetura
O envio de e-mail é definido por uma interface, permitindo desacoplamento do provedor

A implementação atual utiliza AWS SES

A arquitetura facilita a substituição do provedor, evolução do sistema e implementação futura de failover

🔮 Melhorias Futuras
Suporte a múltiplos provedores de e-mail (SendGrid, Mailgun, etc.)

Estratégia de failover automático

Documentação da API com Swagger/OpenAPI

Testes automatizados

Deploy em ambiente cloud (AWS / EC2)

👤 Autor
Desenvolvido por Yago
Backend Developer | Java & Spring Boot

perl
Copiar código

Se você colar isso no `README.md`, **não haverá absolutamente nada fora do arquivo**.  
Se quiser mudar título, nome do projeto ou deixar mais curto, é só falar.
