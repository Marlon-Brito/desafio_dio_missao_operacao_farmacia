<!-- O link para o Modelo de Relatório de Entrega não estava pegando, então formulei o meu próprio -->
# Redução dos Custos em Farmácia com AWS
## Missão Operação Farmacêutica
### Autor
- [@Marlon-Brito](https://github.com/Marlon-Brito)

### Contexto
Empresa farmacêutica que objetiva ser uma revendedora para outras empresas e farmácias que vão de encontro ao cliente final. Sendo um hub de distruibuição de produtos que se comunica com várias outras empresas. E o gestor financeiro não conhece nada sobre Cloud e quer implantar a ferramenta visualizando reduzir custos.

### Tecnologias para solucionar o problema

1. ***Amazon EC2 Auto Scaling***
    - **Redução de custos**: Melhora a gestão de custos e a tolerância a falhas pois identifica as instâncias EC2 da empresa farmacêutica indisponíveis e implanta multi-AZs para prover alta disponibilidade.
    - **Principal ganho**: Escalar a capacidade automaticamente conforme a necessidade do dia (escalabilidade horizontal). Configurando com o tamanho mínimo e máximo de instâncias rodando, a capacidade desejada e até onde pode escalar/aumentar caso precise.

2. ***ELB – Elastic Load Balancing***
    - **Redução de custos**: Para controlar de forma econômica e sem custos o uso das instâncias EC2 na empresa farmacêutica se usará esse processo intermediário, caso contrário ao fazer o Scaling uma instância pode acabar recebendo mais requisições do que as outras, gerando sobrecarregamento do sistema, o que não faz nenhum sentido, ainda mais para o modelo de negócio de uma distribuídora.
    - **Principal ganho**: Balanceamento de carga, sendo um algoritmo que decide para onde vai cada requisição. E caso ocorra redimensionamento de infraestrutura ela redireciona os recursos para as instâncias que ficarem, assim, equilibrando o sistema.


3. ***S3 Intelligent-Tiering***
    - **Redução de custos**: Gerencia automaticamente o ciclo de vida dos objetos 
    armazenados otimizando custos para a empresa farmacêutica. Requesitando apenas uma pequena taxa mensal de monitoramento e automação por objeto.
    - **Principal ganho**: Ideal para dados com padrões de acesso desconhecidos ou em alteração. O que ajudaria muito nesse primeiro momento da ferramenta Cloud AWS na empresa, podendo começar a visualizar as informações geradas e se adaptar a elas.
