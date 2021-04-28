# acqua
### Sistema de Supervisão e Controle de Água

## Introdução

Este repositório contém especificações técnicas para um sistema de supervisão e controle de água de dois reservatórios de 500 m3 cada. Seguem as principais características do esquema atual instalado, cujo croquis está representado a seguir:

![croquis](https://user-images.githubusercontent.com/86032/116254222-8a50cd80-a747-11eb-842a-c8bff6983564.png)

- Os dois reservatórios principais tem 15 m de altura e capacidade para 500 m3 cada um;
- A CEDAE alimenta uma caixa de entrada com capacidade para 10 m3;
- Uma bomba transfere a água da caixa de entrada para os dois reservatórios principais;
- Acredita-se existir tubos de interligação entre os dois tanques para equilibrar o nível da água;
- A distância entre os tanques principais e o quadro da bomba de entrada é de 1 Km;
- Existe um quadro de comando que atua na bomba, a partir da bóia da caixa de entrada;
- A bomba liga sempre que a água na caixa de entrada atinge um certo nível;
- A bomba desliga quando não há água na caixa de entrada;
- A bomba é desligada manualmente se o controle visual do manômetro dos reservatórios principais indica tanque cheio, correspondendo a uma pressão maior que 1.5 kg/cm2;

## Tanques principais e gerador

Reservatórios principais com capacidade de 500 m3

![reservatorios](https://user-images.githubusercontent.com/86032/116251318-f120b780-a744-11eb-9716-656fc5e7cb19.jpg)

Sala do gerador localizado ao lado dos tanques principais

![gerador](https://user-images.githubusercontent.com/86032/116251333-f41ba800-a744-11eb-9652-6bb8ba3cc472.jpg)

## Caixa de entrada

Segue foto da caixa de entrada com capacidade para 10 m3:

![caixa-de-entrada](https://user-images.githubusercontent.com/86032/116251328-f2ea7b00-a744-11eb-973a-74a538368878.jpg)

## Quadros de comando

Seguem fotos dos quadros de comando:

![quadro-1](https://user-images.githubusercontent.com/86032/116251306-ef56f400-a744-11eb-8fef-72a4e3e4ce6f.jpg)
![quadro-2](https://user-images.githubusercontent.com/86032/116251308-efef8a80-a744-11eb-8fa6-ae57d3fa5661.jpg)

## Manômetro dos tanques pricipais

Segue foto do manômetro que equipa cada um dos tanques, a indicação de tanque cheio corresponde à pressão de 1.5 kg/cm2.

![manometro-2](https://user-images.githubusercontent.com/86032/116251300-ee25c700-a744-11eb-877d-5a9cff9f91c5.jpg)

## Sistema de Supervisão e Controle

O Sistema de Supervisão e Controle a ser instalado deverá possuir os seguintes componentes:

- **Central do Sistema**: composto por dois microcomputadores, é responsável por capturar as informações em tempo real e gerar os comandos necessários á operação de abastecimento dos reservatórios;
- **Atuador da bomba**: instalado no quadro de comando da bomba, conecta-se através do link de fibra ótica à Central do Sistema. É o responsável por enviar comandos à bomba;
- **Sensores digitais de pressão**: instalados em ambos os tanques principais, utiliza a tecnologia PoE (Power over Ethernet) para alimentação e comunicação de dados. Conectado à Central do Sistema através de cabos de par trançado.
- **Sensor digital a laser (opcional)**: nesse caso, seria também capturado o nível do tanque de entrada, medido em milímetros, até o limite de 4 metros.

Estes componentes serão interligados através de uma rede local de comunicação padrão Ethernet, com banda passante especificada em 200 Mbps. Está previsto que o Sistema de Supervisão e Controle combine os componentes acima para exercer as funções e/ou características especificadas a seguir.

### Controle

- Instalação de um atuador no quadro de comando da bomba;
- O atuador permitirá um modo automático de operação para ligar/desligar a bomba;
- No modo manual, o sistema se comportará como [antes](https://github.com/SaveH2o/acqua#introdu%C3%A7%C3%A3o);
- No modo automático, a bomba deve desligar quando os reservatórios principais encherem;
- No modo automático, a bomba deve ligar quando a água estiver abaixo de um certo nível;
- Interligação do atuador com a Central de Comando, através de um link de fibra ótica;
- As modificações no quadro de comando serão autorizadas/realizadas pelo cliente; ??

### Supervisão

- Sensores digitais de pressão para cálculo em tempo real do nível da água nos reservatórios;
- Central do Sistema instalada em local abrigado equipado com alimentação no-break;
- Para redundância em caso de falhas, a central será equipada com dois microcomputadores;
- A Central dispõe de telas com indicadores e gráficos relativos ao estado do sistema;
- Indicadores luminosos próximos aos reservatórios e à bomba sinalizam o estado do sistema;
- Sensor laser opcional para obtenção do nível da caixa de entrada em tempo real;
- As instalações de sensores serão autorizadas/realizadas pelo cliente; ??

### Rede Local de Comunicação

- Link de fibra ótica (single-mode/200Mbps) entre os reservatórios e a central de supervisão;
- Links Ethernet (PoE/Cat6/200Mbps) utilizando cabo de par trançado entre a Central do Sistema a cada um dos tanques principais, com comprimento de até 100 m;
- Opcionalmente pode ser utilizada a tecnologia Ethernet Gigabit 1000 Mbps. Nesse caso, seria preservado o investimento em eventual possibilidade de expansão futura do Sistema de Supervisão e Controle para uma quantidade maior de pontos.

### Software

Seguem abaixo duas telas típicas mostradas pela Central do Sistema:

![tela-1](https://camo.githubusercontent.com/39219318bac546815348eb0eb30cde89fd3d88774b966204feb77cc55e4689d2/68747470733a2f2f692e696d6775722e636f6d2f684a47634557572e6a7067)

[tela-2](https://user-images.githubusercontent.com/86032/65999795-84fca580-e474-11e9-9e6e-c87f0e9360c9.png)

Segue um diagrama típico obtido de um Sistema de Supervisão semelhante ao atual, em que a bomba é acionada diversas vezes durante o dia para transferir água da caixa de entrada para o reservatório principal. Durante a madrugada, quando o consumo é baixo, a bomba pode permanecer desligada. Na manhã seguinte, volta novamente a funcionar e toda a variação de estado é registrada.

![gráfico](https://user-images.githubusercontent.com/86032/65921516-d34c6e80-e3b8-11e9-9aca-f2b85e69e5dd.png)
