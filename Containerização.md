# Containerização

* Permite a implantação de aplicações de maneira consistente, repetível e confiável.
* Containerização empacota as dependências junto a aplicação, sendo que, elas não colidirão, já que não compartilham o mesmo sistema de arquivos.


## Questionário para conteneirização

* Quais linguagens a aplicação foi desenvolvida?
* Quais os objetivos se deseja alcançar com a containerização?
* Para implantação da aplicação, estará disponível um implantável(`WAR`, `JAR`, `ZIP`, etc.), ou o código-fonte da aplicação?
* Quais as dependências de desenvolvimento, e serviços consumidos da aplicação?
  * AD(LDAP)
  * Banco de dados - Versão
  * Maven, Composer, NPM, etc
* A aplicação é stateful ou stateless? (A sessão do usuário é guardada)?