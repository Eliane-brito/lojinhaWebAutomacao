# Lojinha WEB Automação
Esse é um repositório que contém a automação de alguns estes em aplicações Web de
um software denominado Lojinha. Os subtópicos abaixo descrevem algumas decisões tomadas na estruturação do projeto.

## Tecnologias Utilizadas

- Java https://www.oracle.com/ae/java/technologies/downloads/
- Junit https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api/5.12.2
- Selenium-Java https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java/4.32.0
- Chrome Driver (Windows Version 64) https://storage.googleapis.com/chrome-for-testing-public/136.0.7103.92/win64/chromedriver-win64.zip

## Testes Automatizados

#### Teste com Page Object
* Criamos o navegador informando que o Chrome será o browser a ser utilizado e navegar para a lojinha
* Maximizar o Browser
* Abrir a página de Login
* Informar o usuário e a senha
* Submeter o formulário de login
* Acessar o formulário de login
* Preencher os dados
* Submeter com erro
* No final apresenta a mensagem toast
* Altere para a mensagem apresentada
* Ao final faça a validação que o texto é o que está dentro da MENSAGEM APRESENTADA.
* Clicar em Adicionar Produto
* Preencher os dados do produto
* Clicar em Salvar
* Apresentará um mensagem toast, peguei esse texto e valido através do assert que o texto é o texto que foi apresentado
* Colocado uma espera implícita na apresentação dessa mensagem toast
* Comando para fechar o navegador

#### Teste de Regras de Negócio

Foram feito testes para validar as partições de equivalência relacionadas ao valor do produto na Lojinha que estão vinculados diretamente a regra de negócio que diz que o valor do produto deve estar entre R$0,01 e R$7.000,00.*


## Notas Gerais

- Utilizamos para refatorar a anotação Before Each e After Each para executar um pedaço do teste antes e outro depois de cada teste para nos dar a flexibilidade de conseguir diminuir a duplicação de código.
- Armazenamos os dados que são enviados para a API através do uso de classes POJO.
- Criamos dados iniciais através do uso de classe Data Factory, para facilitar a criação e controle dos mesmos.
- Nesse projeto fazemos uso do JUnit 5, o que nos dá a possibilidade de usar a anotação  DislayName para dar descrições em Português para nossos testes.
