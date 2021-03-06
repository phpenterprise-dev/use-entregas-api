# Use Entregas API
### Desenvolvido por PHP Enterprise

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
Retorna uma lista de endereços semelhantes 

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| endereco | string | Endereço completo
| numero | string | Número

*Retorna até 10 registros com ID para uso nos métodos "simulate" e "add"

##### POST : /api/simulate
Simula uma entrega.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| tipo            | float      | Local de partida
| pagamento            | float      | Local de chegada
| retorna_origem            | boolean      | Retornar a origem
| enderecos | array | lista de ids por ordem de entrega

##### POST : /api/add
Adiciona uma nova entrega.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| tipo            | float      | Local de partida
| pagamento            | float      | Local de chegada
| retorna_origem            | boolean      | Retornar a origem
| enderecos | array | lista de ids por ordem de entrega

### Atualização regular

@Release 1.0.5

Nota da versão:

Métodos de simulação e registro de solicitação de corrida em teste (versão beta).
