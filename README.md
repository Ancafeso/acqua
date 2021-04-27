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
- O quadro de comando atual é somente entre a bóia da caixa de entrada com o quadro da bomba;
- A bomba só liga se tiver água na caixa de entrada acima de um certo nível;
- A bomba é desligada manualmente quando o controle visual do manômentro indica pressão de tanque cheio, cerca de 15mca ou 1.5 kg/cm2;
- A bomba desliga se não houver água na caixa de entrada;

## Tanques principais

Seguem fotos dos reservatórios principais com capacidade de 500 m3 cada e do gerador que fica ao lado deles:

![reservatorios](https://user-images.githubusercontent.com/86032/116251318-f120b780-a744-11eb-9716-656fc5e7cb19.jpg)
![gerador](https://user-images.githubusercontent.com/86032/116251333-f41ba800-a744-11eb-9652-6bb8ba3cc472.jpg)

## Caixa de entrada

Segue foto da caixa de entrada com capacidade para 10 m3:

![caixa-de-entrada](https://user-images.githubusercontent.com/86032/116251328-f2ea7b00-a744-11eb-973a-74a538368878.jpg)

## Quadros de comando

Seguem fotos dos quadros de comando:

![quadro-1](https://user-images.githubusercontent.com/86032/116251306-ef56f400-a744-11eb-8fef-72a4e3e4ce6f.jpg)
![quadro-2](https://user-images.githubusercontent.com/86032/116251308-efef8a80-a744-11eb-8fa6-ae57d3fa5661.jpg)

## Sistema de Supervisão

O Sistema de Supervisão a ser instalado deverá complementar o sistema atual com as seguintes funções:

- Desligar a bomba automaticamente quando a bóia dos reservatórios principais subir;
- Sensores de pressão para obtenção do nível da água nos reservatórios;
- Sensor a laser (opcional) para obtenção do nível da caixa de entrada;
- Disponibilizar uma central de sistema de supervisão instalada em local abrigado apropriado;
- A central de supervisão deve apresentar telas com indicadores e gráficos relativos ao estado do sistema;
- Indicadores locais (vermelho/amarelo/verde) sinalizam o estado do sistema, próximos aos reservatórios e à bomba;

- Link wireless de comunicação entre os reservatórios, a entrada e a sala de supervisão;

Segue um diagrama típico obtido de um Sistema de Supervisão semelhante ao atual, em que a bomba é acionada diversas vezes durante o dia para transferir água da caixa de entrada para o reservatório principal. Durante a madrugada, onde o consumo é baixo, a bomba permanece desligada. Na manhã seguinte, volta novamente a funcionar e toda a variação de estado é registrada.

![gráfico](https://user-images.githubusercontent.com/86032/65921516-d34c6e80-e3b8-11e9-9aca-f2b85e69e5dd.png)

