# Micro serviços e Monolitos
    
## Micro serviços
    
- Arquiterura Orientada a Serviços (SOA)
- Facilita o desenvolvimento, a integraçao e a manutenção das aplicações
- Requer uma equipe mais qualificada/específica para cada tecnologia utilizada
- Decompoem a aplicação para funções básicas
- Crescimento horizontal
- Cada funcionalidade da aplicação será um serviço independente
- Não comprometer ou depender de outros serviços

## Monolito 

- A modularidade é desejável
- É uma aplicação autônoma e independentede de outras aplicações
- Proporciona a reutilização de código, porem muito cuidado é pouco na hora da manutenção 
- Crescimento vertical
- Basicamente contem a existências de duas camadas DAL (Data Access Layer) e BLL (Business Logic Layer)
- O desenvolvimento pode se tornar complicado a medida que a aplicação cresce
- Dependendo do projeto não requer uma equipe muito grande para o desenvolvimento.

#### Existem padrões de desenvolvimento como DDD (Domain Driven Design), (BDD) (Behavior-driven Design) e TDD (Test-driven Development) para facilitar o desenvolvimento de ambas arquiteturas.

![alt text](https://github.com/eduardoaraya/laravel-and-node-comunication/blob/master/imgs/monolithic-vs-microservices.png)
> https://www.redhat.com/en/topics/microservices/what-are-microservices        


**"Dicas para refatorar um monolito em microserviços - LUIZ FERNANDO DUARTE JUNIOR"** : https://imasters.com.br/apis-microsservicos/dicas-para-refatorar-um-monolito-em-microsservicos
**"Microserviços – Hipsters #17"** : https://hipsters.tech/microservicos-hipsters-17/
**"Microsserviços autônomos na Usabilla – Hipsters On The Road #10"** https://hipsters.tech/microsservicos-autonomos-na-usabilla-hipsters-on-the-road-10/


# Short Polling & Long Polling

### Short Polling
É a definição para quando o frontend envia mutliplas requisições para o backend com intuito de checar se há uma resposta/atualização, sendo assim diminuindo a performance eo desempenho tanto no client-side (requer um processamento contínuo para o envio das requisições) quanto no server-side (sobrecarga no servidor).

![alt text](https://github.com/eduardoaraya/laravel-and-node-comunication/blob/master/imgs/tumblr_lf4hqepXRe1qg976ro1_500.jpg)


### Long Polling 
Basicamente o Front envia somente uma requisição para o backend, mantendo a conexão aberta até sua resposta.
    
# SSE 
"O SSE é um mecanismo que permite ao servidor enviar os dados de forma assíncrona para o cliente assim que a conexão cliente-servidor for estabelecida. O servidor pode então decidir enviar dados sempre que um novo "pedaço" de dados estiver disponível. Pode ser considerado como um modelo de publicação / assinatura unidirecional."
> https://codeburst.io/polling-vs-sse-vs-websocket-how-to-choose-the-right-one-1859e4e13bd9

# WebSocket
"O WebSocket é um protocolo padrão para transferência de dados bidirecional entre um cliente e um servidor.O protocolo webSocket é construído em TCP, não executando em protocolo HTTP.O uso da pesquisa HTTP é extremamente desvantajoso, pois desperdiça recursos e pode causar o tempo limite da conexão." 
> https://dev.to/moz5691/websocket-vs-long-polling-http-412f


# Mão no código!
Agora que ja temos uma breve introdução de micro serviços e socket vamos começar a codar!

## To do list
- [ ] Criar o servidor node
    - [ ] Iniciar um projeto com npm init
    - [ ] Instalar o express
    - [ ] Instalar o socketio
    - [ ] Adicionar um API_KEY para uma middleware específica (O correto é esta chave de api está em um arquivo .env)
    - [ ] Iniciar o servidor na porta 3000

    "const APP_KEY = 'c32d1e78f101470dbcaa4c5e001283509881f3ba4a544521a8c1116ed0a432e2d444c0fc24814b2396d7fd4f9a7cea88'
    app.use( (req, res, next ) => {
        const params = req.body;
        if( params.app_key != app_key ) throw Error('API KEY INVALiD');
        return next();
    });

    const server = app.listen(3000 , () => {
        console.log('Servidor iniciado na porta 3000');
    });"





