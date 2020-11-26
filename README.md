# O que é Docker ?
1 - Não é um sistema de virtualização tradicional (baseado em máquinas virtuais)
Docker não trabalha com esse conceito de máquinas virtuais;

2 - Engine de administração de containers
É um serviço que vai administrar os containers que você vai criar a partir do Docker;
Um container é um processo segregado (isolado) do seu sistema, que a partir daquele processo você pode startar suas aplicações de forma isolado do sistema hospedeiro (host)

3 - Utiliza os serviços do LXC (Linux containers)
Essa tecnologia como o próprio nome diz, ela pertence ao Linux;
Como Docker é baseado no LXC que são os containers, você vai precisar rodar containers baseado em sistemas operacionais Linux

4 - Open source
Docker é uma tecnologia open source e desenvolvido em GO (Linguagem de programação da google)

5 - Sistema de virtualização baseado em software
O kernel da máquina host e compartilhado com o container como algumas outras coisas, por exemplo: bibliotecas, alguns binários da própria maquina host, essa é uma das grandes vantagens do Docker, por isso que ele utiliza muito menos memória, muito mais rápido e ainda assim consegue manter um nível de isolamento extremamente interessante

7 - Empacota software com vários níveis de isolamento
Podemos ter vários níveis de isolamentos com docker.
- Isolamento/Controle na quantidade de memória que um determinado container utiliza;
- Isolamento/Controle na quantidade de CPU que um container utiliza;
- Isolamento/Controle quanto vai poder consumir de rede;
- Ele tem um endereço IP específico dele, então podemos acessar o container a partir de um endereço IP;
- Isolamento do sistema de arquivos, esse isolamento é fundamental para o Docker, os processos que estão dentro do container só poderão escrever no próprio sistema de arquivos.
  
Com todos esses pontos é fundamental para que você consiga colocar seu software dentro de um ambiente controlado sem que haja muita interferências daquilo que esta instalado na máquina host.

# Por que não uma VM?
No Docker temos a maior parte dos benefícios que a máquina virtual tem que é:
- Isolamento do nosso sistema;
- Possibilidade de elasticidade, aumentar e diminuir quantidade de recursos;

A maior vantagem do Docker sobre as máquinas virtuais é a quantidade de recursos que ele consome ao ser executado, por exemplo: A quantidade de recurso de memória que um container requer é absurdamente menor do que a quantidade de memória que por exemplo um sistema operacional inteiro;

[![Container vs Vm](https://github.com/victorreinor/o-que-e-docker/container-vs-vm.jpg "Container vs Vm")](https://github.com/victorreinor/o-que-e-docker/container-vs-vm.jpg "Container vs Vm")

# LXC vs Docker

A tecnologia LXC ela já existia e ela era fantástica, grande dificuldade era o seu uso que precisava de um conhecimento muito específico e aprofundado para que pudesse usar essa tecnologia de uma forma mais útil, o crescimento do Docker está ai para comprovar que essa tecnologia é fantástica.
O Docker faz é: "criar um interface amigável" e toda uma estrutura ao redor do Docker para te dar um suporte desta tecnologia e existe varias ferramentas e formas de interagir

[![LXC vs Docker](https://github.com/victorreinor/o-que-e-docker/lxc-vs-docker.jpg "LXC vs Docker")](https://github.com/victorreinor/o-que-e-docker/lxc-vs-docker.jpg "LXC vs Docker")

# O que é container?
- Segregação de processos no mesmo Kernel (Isolamento);
- Sistema de arquivos criados a partir de uma imagem;
- Ambientes leve e portáteis no qual aplicação são executados;
- Encapsula todos os binários e bibliotecas necessárias para execução de um App;
  

# O que é imagens?
- Modelo de sistema de arquivo somente-leitura usado para criar containers;
  - A imagem docker é justamente o modelo de sistema de arquivos que vai ser usado na hora de criar o container, ele precisa de uma imagem para que ele possa ser criado;
- Imagens são criadas através de um processo chamado build;
- São armazenadas em repositórios no Registry (Docker Hub);
- São compostas por uma ou mais camadas (layers);
- Uma camada representa uma ou mais mudanças no sistema de arquivo; 
- Uma camada é também chamada de imagem intermediária;
- A Junção dessas camadas formam a imagem;
- A apenas a última camada pode ser alterada quando o container for iniciado;
- O grande objetivo dessa estratégia de dividir uma imagem em camadas é o re-uso;
- É possível compor imagens a partir de camadas de outras imagens;

# Container vs Imagem