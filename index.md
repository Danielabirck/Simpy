## **Simpy**

SimPy (Simulation in Python) é um framework1 para a construção de modelos de simulação de eventos discretos em Python e distribuído segundo a licença MIT.Pode-se construir também, além de modelos de simulação discreta, modelos de simulação em “Real Time”, modelos de agentes e até mesmo modelos de simulação contínua.
  
### Instalação

 Alguns programas e bibliotecas são úteis para a instalação do SimPy, são eles: Python, Pip, IDE e Numpy. Eles servem para facilitar as codificações, aumentar a produtividade em Python, entre outros.
 Uma dica é instalar a distribuição gratuita do Anaconda, em que mais de 200 pacotes são instalados simultaneamente, otimizando o processo de instalações.

### Conceitos Básicos

Simpy é uma biblioteca de simulação em que todos os processos estão em um ambiente. Ou seja, os processos interagem entre si e com o ambiente através de eventos.
Os processos são descritos por geradores Python simples. Você pode chamá-los de função de processo ou método de processo, dependendo se é uma função normal ou método de uma classe. Durante sua vida, eles criam eventos e os geram para esperar que sejam acionados.
Quando um processo produz um evento, o processo é suspenso. O SimPy retoma o processo, quando o evento ocorre (dizemos que o evento é acionado). Vários processos podem esperar pelo mesmo evento. O SimPy os retoma na mesma ordem em que geraram aquele evento.
Um tipo de evento importante é o _timeout_. Eventos desse tipo são acionados após um determinado período de tempo (simulado).

Inicialmente, serão necessárias duas bibliotecas do Python: a _random_ – biblioteca de geração de números aleatórios – e a _simpy_, que é o próprio SimPy.

- import random              # gerador de números aleatórios
- import simpy               # biblioteca de simulação

- random.seed(1000)         # semente do gerador de números aleatórios

Tudo no SimPy gira em torno de eventos gerados por funções e todos os eventos devem ocorrer em um environment, ou um “ambiente” de simulação criado a partir da função simpy.Environment().

- import random             # gerador de números aleatórios
- import simpy              # biblioteca de simulação

- random.seed(1000)         # semente do gerador de números aleatórios
- env = simpy.Environment() # cria o environment do modelo na variável 

### Resumo dos Conceitos

- env = simpy.Environment() - cria um Environment de simulação
- random.expovariate(lambd) - gera números aleatórios exponencialmente distribuídos, com taxa de ocorrência (eventos/unidade de tempo) igual a lambd
- yield env.timeout(time) - gera um atraso dado por time
- random.seed(seed) - define o gerador de sementes aleatórias para um mesmo valor a cada nova simulação
- env.process(geraChegadas(env)) - inicia a função geraChegadas como um processo em env
- env.run(until=tempoSim) - executa a simulação (executa todos os processos criados em env) pelo tempo tempoSim
- env.now - retorna o instante atual da simulação


### Por que utilizar o SimPy?

- Facilidade de codificação
- Um grande número de bibliotecas
- Scripts

Sob o aspecto funcional, SimPy se apresenta como uma biblioteca em Python e isso significa que um modelo de simulação desenvolvido com ele, terá à disposição tudo que existe de bom para quem programa em Python: o código fica fácil de ler (e desenvolver), o modelo pode ser distribuído como um pacote (sem a necessidade do usuário final instalar o Python para executá-lo), além das diversas bibliotecas de estatística e otimização disponíveis em Python, que ampliam, em muito, o horizonte de aplicação dos modelos.

Esta disponibilidade de bibliotecas, bem como ser um software livre, torna o SimPy particularmente interessante para quem está desenvolvendo sua pesquisa acadêmica na área de simulação. O seu modelo provavelmente ficará melhor documentado e portanto mais fácil de ser compreendido, potencializando a divulgação dos resultados de sua pesquisa em dissertações, congressos e artigos científicos.


## Prós e Contras

### Prós
- Código aberto e livre (licença MIT);
- Diversas funções de bibliotecas de otimização, matemática e estatística podem ser incorporadas ao modelo;
-Permite a programação de lógicas sofisticadas, apoiando-se no Python (e suas bibliotecas);
-Comunidade ativa de desenvolvedores e usuários que mantém a biblioteca atualizada;

### Contras
- Ausência de ferramentas para animação;
- Necessidade de se programar cada processo do modelo;
- Exige conhecimento prévio em Python;
- Não inclui um ambiente visual de desenvolvimento.








