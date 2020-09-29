# Use Entregas API
### Desenvolvido por Php Enterprise

API e documentação de comunicação com a plataforma [Use Entregas](http://useentregas.com.br).

Direitos reservados à Use Soluções em Entregas e Tecnologia Ltda.

### Tornar-se parceiro

Para você usar a API e se tornar um parceiro, será necessário solicitar a criação de uma chave de usuário à [Use Entregas](http://useentregas.com.br).

### Endereço da API (url)

https://useentregas.com.br/api

### Autenticação

Método Baurer

##### Parâmetros do header na chamada:

<i>Content-Type: Application/JSON
  
  Authorization: Bearer {usertoken}</i>

### Tipos de métodos

##### GET : api/

Permite testar se conectou-se com sucesso à API.

##### GET : api/list

Lista todas as entregas.

##### Tradução de campos:

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| id            | integer      | Id da entrega
| cadastro            | datetime      | Data e hora do cadastro
| distancia            | float      | Distância da entrega
| valor_corrida            | float      | Valor total da corrida
| valor_boy            | float      | Valor para o motoboy
| valor_use            | float      | Valor para a Use Entregas
| data_entrega            | datetime      | Data e hora da entrega
| tipo            | string      | Tipo da entrega: 1 = simples, 2 = malote, 3 = banco, 4 = cartório
| pagamento            | string      | Tipo de pagamento
| status            | string      | Status da entrega: 1 = procurando entregador, 2 = em andamento, 3 = cancelada, 9 = concluída
| observacao            | string      | Observações
| enderecos | array | Listagem de endereços (vide tabela abaixo) 

##### Endereços:

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| endereco | string | Endereço completo
| numero | string | Número
| lat | float | Latitude
| lng | float | Longitude
| complemento | string | Complemento
| ordem | string | Ordem da entrega, local 1 é a origem.

##### GET : /api/delivery/:id

Lista os detalhes de uma entrega específica.

##### Tradução de campos:

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| id            | integer      | Id da entrega
| cadastro            | datetime      | Data e hora do cadastro
| distancia            | float      | Distância da entrega
| valor_corrida            | float      | Valor total da corrida
| valor_boy            | float      | Valor para o motoboy
| valor_use            | float      | Valor para a Use Entregas
| data_entrega            | datetime      | Data e hora da entrega
| tipo            | string      | Tipo da entrega: 1 = simples, 2 = malote, 3 = banco, 4 = cartório
| pagamento            | string      | Tipo de pagamento
| status            | string      | Status da entrega: 1 = procurando entregador, 2 = em andamento, 3 = cancelada, 9 = concluída
| observacao            | string      | Observações
| enderecos | array | Listagem de endereços (vide tabela abaixo) 

##### Endereços:

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| endereco | string | Endereço completo
| numero | string | Número
| lat | float | Latitude
| lng | float | Longitude
| complemento | string | Complemento
| ordem | string | Ordem da entrega, local 1 é a origem.

##### POST : /api/address
Encontra o código do endereço.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| place_id            | string      | Código do endereço
| formatted_address            | string      | Endereço completo
| lat            | float      | Latitude
| lng            | float      | Longitude

##### POST : /api/simulate
Simula uma entrega.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código


##### POST : /api/add
Adiciona uma nova entrega.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código
| id            | integer      | código


### Atualização regular

@Release 0.1

Nota da versão:

Nenhuma.
