# Sensor de irrigação e fertirrigação automatica por ESP32 - FIAP

Projeto do curso de inteligencia artificial da turma 1TIAOR da faculdade FIAP.
Esse projeto tem como função simular a automatização da irrigação e do equilibrio do PH do solo atraves da adulbação com NPK, atraves de sensores, tendo como modelo um plantio de milho e seus parametros segundo Embrapa.
Para essa simulação foram usados valores estabelecidos de forma manual para simular o funcionamento do sensor DHT22, que por sua vez considera a umidade como sendo do solo e não como umidade relativa do ar no qual ele foi projetado para medir.
Foi utilizado um sensor LDR que originalmente é usado para medir luminosidade no ambiente, para medir valores simulados de PH determinados por tres botões verdes cada um representando um elemento Nitrogenio (N), Fósforo (P) e Potassio (K), onde cada um representa desequilibrio no PH quanto pressionado.
O relé tem como função ligar uma bomba de irrigação que pode ser alimentada somente para irrigação ou tambem para fertirrigação, a bomba é representada pelo LED azul que quando acesso indica que esta sendo irrigado ou fertirrigado e apagado que indica que tudo está de acordo com as especificações e a bomba esta desligada.
Os sensores são ligados pela placa ESP32 seguindo os respectivos padrões de pinagem e foi usado o site wokwi.com para a simulação e compilação do projeto.
Em resulmo o projeto inicia com uma umidade equivalente de 0% e atraves da digitação no modelo "U=65.00", você determina a umidade que quer simular, como no exemplo 65% , caso esteja abaixo de 70% será acionado o relé e o LED, junto a isso aparecerá uma menssagem alertando a baixa umidade e indicando que a irrigação está sendo feita.
Ao apertar qualquer um dos três botões verdeds ele tambem irá aparecer uma menssagem alertando o desequilibrio do PH e ligando a fertirrigação, simulando uma dosagem de insumo junto a agua para o ajuste do PH (PH do milho que tem como numero ideal 6,5 mas no exemplo usamos o valor 1000 para indicar o valor ideal).







