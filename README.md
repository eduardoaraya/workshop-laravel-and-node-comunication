# Introdução a microserviços e monolitos
    
    ## Microserviços
        
        - Arquiterura Orientada a Serviços (SOA)
        - Facilita o desenvolvimento, a integraçao e a manutenção das aplicações
        - Requer uma equipe mais qualificada/específica para cada tecnologia utilizada
        - Decompoem a aplicação para funções básicas
        - Crescimento horizontal
        - Cada funcionalidade da aplicação será um serviço independente
        - Não comprometer ou depender de outros serviços

    ## Monolitos 

        - A modularidade é desejável
        - É uma aplicação autônoma e independentede de outras aplicações
        - Proporciona a reutilização de código, porem muito cuidado é pouco na hora da manutenção 
        - Crescimento vertical
        - Basicamente contem a existências de duas camadas DAL (Data Access Layer) e BLL (Business Logic Layer)
        - O desenvolvimento pode se tornar complicado a medida que a aplicação cresce
        - Dependendo do projeto não requer uma equipe muito grande para o desenvolvimento.

        ![alt text](https://github.com/eduardoaraya/laravel-and-node-comunication/blob/master/monolithic-vs-microservices.png)
        
    #### Existem padrões de desenvolvimento como DDD (Domain Driven Design), (BDD) (Behavior-driven Design)
    e TDD (Test-driven Development) para ambas arquiteturas.

    ### **"Dicas para refatorar um monolito em microserviços - LUIZ FERNANDO DUARTE JUNIOR" **: https://imasters.com.br/apis-microsservicos/dicas-para-refatorar-um-monolito-em-microsservicos
    ### **"Microserviços – Hipsters #17" : https://hipsters.tech/microservicos-hipsters-17/
    ### **"Microsserviços autônomos na Usabilla – Hipsters On The Road #10"** : https://hipsters.tech/microsservicos-autonomos-na-usabilla-hipsters-on-the-road-10/


# Short Polling & Long Polling / HTTP

    ## Short Polling
        É a definição para quando o frontend envia mutliplas requisições para o backend com intuito de 
        checar se há uma resposta/atualização. Assim diminuindo o desempenho e performace
        tanto no client-side quanto no server-side que fica sobrecarregado.

    ## Long Polling 
        Basicamente o Front envia somente uma requisição para o backend, mantendo a conexão aberta até sua resposta.
       

# WebSocket
    -  WebSocket
        "O WebSocket é um protocolo padrão para transferência de dados bidirecional entre um cliente e um servidor. 
        O protocolo webSocket é construído em TCP, não executando em protocolo HTTP. 
        O uso da pesquisa HTTP é extremamente desvantajoso, pois desperdiça recursos e pode causar o tempo limite da conexão."
        https://dev.to/moz5691/websocket-vs-long-polling-http-412f



