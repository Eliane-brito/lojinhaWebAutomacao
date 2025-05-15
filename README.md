# 🧪 Lojinha Web - Projeto de Automação de Testes

Este repositório contém a automação de testes para a aplicação web **Lojinha**. O objetivo é validar funcionalidades e regras de negócio da aplicação utilizando boas práticas como Page Object Model, JUnit 5 e Selenium WebDriver.

---

## 🚀 Tecnologias Utilizadas

- [Java](https://www.oracle.com/ae/java/technologies/downloads/)
- [JUnit 5](https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api/5.12.2)
- [Selenium WebDriver](https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java/4.32.0)
- [ChromeDriver (Windows 64)](https://storage.googleapis.com/chrome-for-testing-public/136.0.7103.92/win64/chromedriver-win64.zip)

---

## ✅ Testes Automatizados

### 🔸 Testes com Page Object

- Configuração do navegador Chrome como browser principal.
- Maximização da janela do navegador.
- Acesso à página de login.
- Preenchimento de credenciais (usuário e senha).
- Submissão do formulário de login.
- Acesso ao formulário de adição de produto.
- Preenchimento de dados incorretos para simulação de erro.
- Validação da mensagem de erro (*toast*) exibida.
- Preenchimento de dados válidos para cadastro de produto.
- Submissão do formulário e validação da mensagem de sucesso.
- Uso de **espera implícita** para aguardar a exibição da mensagem.
- Encerramento do navegador ao final dos testes.

### 🔸 Testes de Regras de Negócio

- Validação das **partições de equivalência** relacionadas ao valor do produto.
- Regra de negócio: o valor do produto deve estar entre **R$ 0,01 e R$ 7.000,00**.
- Verificação de comportamentos esperados em cenários válidos e inválidos.

---

## 🛠️ Boas Práticas e Arquitetura

- Uso de `@BeforeEach` e `@AfterEach` para execução de trechos de código antes e depois de cada teste, promovendo reutilização e legibilidade.
- Criação de dados dinâmicos com uma **classe Data Factory**, facilitando a geração e manutenção dos dados de teste.
- Armazenamento dos dados usando classes simples (**POJOs**), organizando os objetos de entrada.
- Utilização da anotação `@DisplayName` do JUnit 5 para descrever os testes em **português**, melhorando a documentação dos testes.

---

## 💡 Considerações Finais

Este projeto foi desenvolvido com fins educacionais e de prática profissional em automação de testes web. Novas funcionalidades e melhorias poderão ser implementadas conforme a evolução do projeto.

