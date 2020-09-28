# Use Entregas API
### Desenvolvido por Php Enterprise

API e documentação de comunicação com a plataforma [Use Entregas](http://useentregas.com.br).

Direitos reservados à [Php Enterprise](http://useentregas.com.br) Soluções em Software Ltda.

### Requísitos 

* PHP 5.3 ou superior
* Apache 2.2+

### Autenticação

Método Baurer

Ex: !!!!!tokem no cabeçalho!!

### Acesso direto (url)

    https://useentregas.com.br/api

* {usuario}  = usuário do ws
* {chave}    = chave do ws

### Uso em ambiente de produção

Será necessário a criação de um login, chave de acesso e a liberação do endereço de IP (servidor onde a API será executada).

### Exemplo de uso

...

### Tipos de métodos

##### GET : /api/list/
Lista todas as entregas.

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
| pagamento            | string      | 
| status            | string      | Status da entrega: 1 = procurando entregador, 2 = em andamento, 3 = cancelada, 9 = concluída
| observacao            | string      | Observações
| enderecos | array | Listagem de endereços

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| endereco | string | Endereço completo
| numero | string | Número
| lat | float | Latitude
| lng | float | Longitude
| complemento | string | Complemento
| ordem | string | Ordem da entrega, local 1 é a origem.











##### GET : /api/rider/:id
Lista todas as entregas de um determinado entregador.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| Id            | integer      | Id da entrega
| TokenUser            | string      | Código do usuário
| TipoEntrega1            | string      | Tipo da entrega: 1 = simples, 2 = malote, 3 = banco, 4 = cartório
| DistanciaBoyEntrega            | float      | VERIFICAR!!
| DistanciaTotalMelhorRota            | float      | Distância da entrega
| AgendarEntrega            | datetime      | Data e hora do agendamento da entrega
| Observacao            | string      | Observações
| TokenDesconto            | string      | VERIFICAR!!
| ValorCorrida            | float      | Valor total da corrida
| ValorBoy            | float      | Valor para o motoboy
| ValorUse            | float      | Valor para a Use Entregas
| DthCad            | datetime      | Data e hora do cadastro da entrega
| IdBoyAceitou            | string      | Código do motoboy que aceitou a entrega
| TipoPagamento            | integer      | Tipo de pagamento: VERIFICAR!!
| StatusEntrega            | string      | Status da entrega: 1 = procurando entregador, 2 = em andamento, 3 = cancelada, 9 = concluída
| StatusPagamento            | integer      | Status do pagamento: VERIFICAR!!
| TokenPagamento            | string      | VERIFICAR!!
| DthPagamento            | datetime      | Data e hora do pagamento
| Teste            | integer      | VERIFICAR!!
| TokenRel            | string      | VERIFICAR!!

##### GET : /api/delivery/:id
Lista os detalhes de uma entrega específica.

| campo         | tipo         |  descrição  |
| ------------- | ------------ | ------------- |
| Id            | integer      | Id da entrega
| TokenUser            | string      | Código do usuário
| TipoEntrega1            | string      | Tipo da entrega: 1 = simples, 2 = malote, 3 = banco, 4 = cartório
| DistanciaBoyEntrega            | float      | VERIFICAR!!
| DistanciaTotalMelhorRota            | float      | Distância da entrega
| AgendarEntrega            | datetime      | Data e hora do agendamento da entrega
| Observacao            | string      | Observações
| TokenDesconto            | string      | VERIFICAR!!
| ValorCorrida            | float      | Valor total da corrida
| ValorBoy            | float      | Valor para o motoboy
| ValorUse            | float      | Valor para a Use Entregas
| DthCad            | datetime      | Data e hora do cadastro da entrega
| IdBoyAceitou            | string      | Código do motoboy que aceitou a entrega
| TipoPagamento            | integer      | Tipo de pagamento: VERIFICAR!!
| StatusEntrega            | string      | Status da entrega: 1 = procurando entregador, 2 = em andamento, 3 = cancelada, 9 = concluída
| StatusPagamento            | integer      | Status do pagamento: VERIFICAR!!
| TokenPagamento            | string      | VERIFICAR!!
| DthPagamento            | datetime      | Data e hora do pagamento
| Teste            | integer      | VERIFICAR!!
| TokenRel            | string      | VERIFICAR!!

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
