Escolha da Estrutura

A estrutura escolhida foi o Express.js (Node.js). Essa alternativa foi a mais apropriada devido aos seguintes motivos:
Possui flexibilidade e simplicidade, ideal para desenvolver APIs REST rapidamente.
Oferece um ecossistema bastante robusto, com middlewares prontos para CORS, segurança (helmet), logging (morgan), autenticação e muito mais.
É bastante comum no ambiente profissional, facilitando a manutenção por outros programadores.
Para a situação determinada (API de pedidos com autenticação, monitoramento e controle de acesso), o Express permite uma implementação eficaz, clara e facilmente ampliável.

Integração com Serviço de Terceiros

No código otimizado, ao invés de utilizar um SDK externo como o OpenRouteService, realizamos uma conexão com o sistema de CORS e acessamos a API através do fetch (no cliente).
O navegador/front-end que faz uso da API é o serviço externo implementado aqui. Para isso, configuramos o CORS (Cross-Origin Resource Sharing) com diretrizes específicas, permitindo apenas requisições de http://frontend.secureflow.com.
Além disso, aplicamos autenticação baseada em token (Bearer meutokensecreto123) para garantir que apenas usuários permitidos possam acessar informações confidenciais (/pedidos).

Dependências

Pacotes que foram instalados no projeto:
express → framework para a criação de servidores e rotas HTTP.
cors → configuração das regras de Cross-Origin Resource Sharing, restringindo o acesso à API a origens autorizadas.
Essas dependências foram adicionadas através do npm e estão documentadas no arquivo package.json.
