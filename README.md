# Lojinha WEB Automação

Esse é um repositório que contém a automação de alguns testes em aplicações Web de um software denominado **Lojinha**. Os subtópicos abaixo descrevem algumas decisões tomadas na estruturação do projeto.

---

## Tecnologias Utilizadas

- [Java](https://www.oracle.com/ae/java/technologies/downloads/)
- [JUnit 5](https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api/5.12.2)
- [Selenium-Java](https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java/4.32.0)
- [Chrome Driver (Windows Version 64)](https://storage.googleapis.com/chrome-for-testing-public/136.0.7103.92/win64/chromedriver-win64.zip)

---

## Testes Automatizados

### Teste com Page Object

- Criamos o navegador informando que o Chrome será o browser a ser utilizado e navegamos para a aplicação Lojinha.
- Maximizamos o browser.
- Abrimos a página de login.
- Informamos o usuário e a senha.
- Submetemos o formulário de login.
- Acessamos o formulário de adição de produto.
- Preenchemos os dados e submetemos com erro.
- A mensagem *toast* é exibida.
- Realizamos a validação de que o texto apresentado corresponde à mensagem esperada.
- Clicamos em **Adicionar Produto**.
- Preenchemos os dados do produto.
- Clicamos em **Salvar**.
- A mensagem *toast* é validada com `assert`, garantindo que o texto exibido é o esperado.
- Foi colocada uma **espera implícita** para a apresentação dessa mensagem.
- Por fim, fechamos o navegador.


### Teste de Regras de Negócio

Foram realizados testes para validar as **partições de equivalência** relacionadas ao valor do produto na Lojinha, que está vinculado diretamente à **regra de negócio** que determina que o valor do produto deve estar entre **R$0,01 e R$7.000,00**.

---

## Notas Gerais

- Utilizei as anotações `@BeforeEach` e `@AfterEach` para executar trechos de código antes e depois de cada teste, reduzindo a duplicação.
- Armazenei os dados enviados para a API usando classes **POJO**.
- Criei dados iniciais com o uso de uma **classe Data Factory**, facilitando sua criação e controle.
- Utilizei **JUnit 5**, o que nos permite usar a anotação `@DisplayName` para descrever os testes em português.

---


