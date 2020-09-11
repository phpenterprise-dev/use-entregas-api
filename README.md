# Use Entregas API
### Desenvolvida por Php Enterprise

API e documentação de comunicação com a plataforma [Use Entregas](http://useentregas.com.br).

[![GPL Licence](https://badges.frapsoft.com/os/gpl/gpl.svg?v=103)](https://opensource.org/licenses/MIT/) [![PHPPackages Rank](http://phppackages.org/p/smartdealer/sdapi/badge/rank.svg)](http://phppackages.org/p/smartdealer/sdapi) ![](https://reposs.herokuapp.com/?path=smartdealer/sdapi&style=flat)

Direitos reservados à Php Enterprise Soluções em Software Ltda.

### Requísitos 

* PHP 5.3 ou superior
* Apache 2.2+

### Autenticação

...

### Acesso direto (url)

    https://{usuario}:{chave}@useentregas.com.br

* {usuario}  = usuário do ws
* {chave}    = chave do ws

### Uso em ambiente de produção

Será necessário a criação de um login, chave de acesso e a liberação do endereço de IP (servidor onde a API será executada).

### Exemplo de uso

...

### Tipos de métodos

##### GET : /api/list/
Lista todas as entregas

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| id            | integer      | código


##### GET : /api/rider/:id
Lista todas as entregas de um determinado entregador

Breve exemplo, para ver a lista completa faça uma chamada a rota Rest acima.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| id            | integer      | código

##### POST : /api/delivery/:id
Lista os detalhes de uma entrega específica.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| id            | integer      | código

##### POST : /api/simulate
Simula uma entrega.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| id            | integer      | código

##### POST : /api/add
Adiciona uma nova entrega.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| id            | integer      | código


### Atualização regular

@Release 0.1

Nota da versão:

Nenhuma.
