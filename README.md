# cherry
Um robô hexapod controlado por uma ESP32 automático ou remotamente. Nossa cereja.
A Cherry é uma hexapod desenvolvida como uma evolução da Tiffany e da Scarlet. O intuito é adicionar uma IMU e mover a bateria para o interior do robô. A Cherry pode andar de forma autônoma, ser controlada pelo celular ou pelo nosso espaço inteligente por MQTT. Para se locomover, ela possui 6 patas de 3 graus de liberdade cada (3 motores) e uma ESP32 que comanda o conjunto! Ela é a nossa cereja, a irmã da Tiffany e da Scarlet e a nova integrante robótica do nosso espaço inteligente!

# Estrutura física
A estrutura física do robô é composta por seis patas de três eixos cada (três motores). As patas são fixadas a duas placas de PLA para deixar o robô firme. As peças são todas projetadas em 3D e foram impressas utilizando PLA, podendo ser encontradas na pasta "parts" deste projeto.

<img src="https://github.com/Penguin-Lab/cherry/blob/main/images/cherry0.png" height="250"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/cherry2.png" width="350"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/cherry1.png" width="350">

## Peças 3D em STL
As peças em 3D desenvolvidas para este projeto foram baseadas nos projetos das hexapods Tiffany e Scarlet. Na pasta "parts", estão listadas essas peças em STL. Para ajudar, segue abaixo uma lista de todas as peças que devem ser impressas e qual o valor da sua maior dimensão (para ajudar na escolha da impressora):

* Corpo
  * 1x [CHERRY_BODY_DOWN.STL (230 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BODY_DOWN.STL)
  * 1x [CHERRY_BODY_UP.STL (230 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BODY_UP.STL)
  * 1x [CHERRY_BODY_UP_BLOSSOMS.STL (113 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BODY_UP_BLOSSOMS.STL)
  * 1x [CHERRY_BODY_UP_BRANCH.STL (96 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BODY_UP_BRANCH.STL)
  * 1x [CHERRY_BODY_UP_LEAVES.STL (168 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BODY_UP_LEAVES.STL)
  * 1x [CHERRY_LOGO.STL (36 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_LOGO.STL)
  * 2x [CHERRY_SPACER_FRONT.STL (33 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SPACER_FRONT.STL)
  * 2x [CHERRY_SPACER_CENTER.STL (64 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SPACER_CENTER.STL)
  * 1x [CHERRY_BATTERY_CASE.STL (164 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BATTERY_CASE.STL)
  * 1x [CHERRY_BATTERY_DOOR.STL (77 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BATTERY_DOOR.STL)
  * 1x [CHERRY_SUPORT_PLUGS_SWITCHES.STL (50 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SUPORT_PLUGS_SWITCHES.STL)
  * 1x [CHERRY_SUPORT_PLUGS_BATTERY.STL (67 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SUPORT_PLUGS_BATTERY.STL)
* Patas
  * 6x [CHERRY_TIBIA_LEFT.STL (171 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_TIBIA_LEFT.STL)
  * 6x [CHERRY_TIBIA_RIGHT.STL (171 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_TIBIA_RIGHT.STL)
  * 6x [CHERRY_TIBIA_MIDDLE.STL (61 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_TIBIA_MIDDLE.STL)
  * 3x [CHERRY_SHIELD_A_LEFT.STL (145 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SHIELD_A_LEFT.STL)
  * 3x [CHERRY_SHIELD_A_RIGHT.STL (145 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SHIELD_A_RIGHT.STL)
  * 3x [CHERRY_SHIELD_B_LEFT.STL (145 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SHIELD_B_LEFT.STL)
  * 3x [CHERRY_SHIELD_B_RIGHT.STL (145 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SHIELD_B_RIGHT.STL)
  * 6x [CHERRY_FOOT.STL (25 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_FOOT.STL)
  * 3x [CHERRY_FEMUR_FRONT_LEFT.STL (132 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_FEMUR_FRONT_LEFT.STL)
  * 3x [CHERRY_FEMUR_FRONT_RIGHT.STL (132 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_FEMUR_FRONT_RIGHT.STL)
  * 3x [CHERRY_FEMUR_BACK_LEFT.STL (132 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_FEMUR_BACK_LEFT.STL)
  * 3x [CHERRY_FEMUR_BACK_RIGHT.STL (132 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_FEMUR_BACK_RIGHT.STL)
  * 6x [CHERRY_FEMUR_MIDDLE.STL (51 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_FEMUR_MIDDLE.STL)
  * 6x [CHERRY_OMBRO_DOWN.STL (97 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_OMBRO_DOWN.STL)
  * 3x [CHERRY_OMBRO_UP_LEFT.STL (97 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_OMBRO_UP_LEFT.STL)
  * 3x [CHERRY_OMBRO_UP_RIGHT.STL (97 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_OMBRO_UP_RIGHT.STL)
* Motor
  * 12x [CHERRY_TAMPA_MOTOR_DS3230.STL (40 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_TAMPA_MOTOR_DS3230.STL)

Obs: a tampa de 12 motores deverão ser trocadas pelas peças [CHERRY_TAMPA_MOTOR_DS3230.STL (41 mm)](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_TAMPA_MOTOR_DS3230.STL) para que seja possível fixar os rolamentos nas patas. Serão utilizados 3 rolamentos por pata:

<img src="https://github.com/Penguin-Lab/cherry/blob/main/images/pata0.png" height="300"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/pata1.png" height="300"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/corpo0.png" height="300"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/corpo1.png" height="300">

Obs 2: os motores ficam fixados nas peças por [discos metálicos pequenos padrão para eixos de servo](https://a.aliexpress.com/_mPHt3nf).

<img src="https://github.com/Penguin-Lab/lilla/blob/main/images/discoeixo.png" height="100">

<img src="https://github.com/Penguin-Lab/cherry/blob/main/images/pata2.png" height="300"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/pata3.png" height="300"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/corpo2.png" height="300"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/corpo3.png" height="300">

## Outros itens da estrutura
Alguns outros itens são necessários para finalizar a estrutura da Cherry:
* 6x Parafusos m4 de 90 mm com porca autotravante: fechar o robô prendendo as peças [CHERRY_BODY_UP.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BODY_UP.STL), [CHERRY_BODY_DOWN.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BODY_DOWN.STL), [CHERRY_SPACER_FRONT.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SPACER_FRONT.STL), [CHERRY_SPACER_CENTER.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SPACER_CENTER.STL), [CHERRY_BATTERY_CASE.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BATTERY_CASE.STL), [CHERRY_BATTERY_DOOR.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BATTERY_DOOR.STL), [CHERRY_SUPORT_PLUGS_SWITCHES.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SUPORT_PLUGS_SWITCHES.STL) e [CHERRY_SUPORT_PLUGS_BATTERY.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_SUPORT_PLUGS_BATTERY.STL)
* 24x Parafusos m4 de 55 mm com porca: fechar os ombros prendendo as peças [CHERRY_OMBRO_DOWN.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_OMBRO_DOWN.STL) com as peças [CHERRY_OMBRO_UP_LEFT.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_OMBRO_UP_LEFT.STL) e [CHERRY_OMBRO_UP_RIGHT.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_OMBRO_UP_RIGHT.STL)
* 12x Parafusos m4 de 50 mm com porca: fechar os ombros prendendo as peças [CHERRY_OMBRO_DOWN.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_OMBRO_DOWN.STL) com as peças [CHERRY_OMBRO_UP_LEFT.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_OMBRO_UP_LEFT.STL) e [CHERRY_OMBRO_UP_RIGHT.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_OMBRO_UP_RIGHT.STL)
* Diversos parafusos m3
* 6x Tiras de EVA: colocar na ponta das peças [CHERRY_FOOT.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_FOOT.STL) para evitar que o robô deslize
* Arruelas entre as porcas e a peça [CHERRY_BODY_DOWN.STL](https://github.com/Penguin-Lab/cherry/blob/main/parts/CHERRY_BODY_DOWN.STL)

## Placa de circuito impresso
No projeto, foi desenvolvida uma placa de circuito para servir como shield para a ESP32 e conexão com um hub i2c (que conecta as duas placas PCA9685 e a IMU ao microcontrolador), com o DFPlayer Mini MP3 Player, com o calibrador de motores e com a fita de cobre (como sensor de toque do robô).

<img src="https://github.com/Penguin-Lab/cherry/blob/main/images/circuit0.png" width="350"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/circuit1.png" width="350">

<img src="https://github.com/Penguin-Lab/cherry/blob/main/images/board0.png" height="500"> <img src="https://github.com/Penguin-Lab/cherry/blob/main/images/board1.png" height="500">

## Calibração dos motores
A calibração dos motores é feita utilizando o [CALIBRADOR DE MOTORES](https://github.com/Penguin-Lab/calib_servomotor) conectado às PCAs da Cherry. Isso deve ser feito pelo clock das PCAs ser diferente de uma placa para outra. Logo, os motores da esquerda são calibrados utilizando a PCA da esquerda e os da direita com a PCA da direita. Os valores retornados pela calibração são jogados nesta [PLANILHA](https://docs.google.com/spreadsheets/d/1Kh9AVbb79lXnJq5dlCiB7NEVVmcJWRX6X2CdDR9_QZo/edit?gid=885718543). A planilha ajeita os valores de PWM retornados na IDE do Arduino para valores que representem 0 e 180 graus dos motores já na estrutura das patas. Esses valores são os mesmos listados no código de comando da Cherry.

## Componentes eletrônicos
Os componentes eletrônicos embarcados no robô e equipamentos utilizados estão listados abaixo.
* Controlador com Wi-fi e Bluetooth
  * 1x ESP32 (38 pinos)
* Motores
  * 18x Servo DS3230 PRO-180
* 2x Placas PCA9685 para comando dos 18 motores (9 motores em cada)
* Chave (switch)
* Chave pequena (switch)
* Alimentação
  * Regulador para 5V (ESP32)
  * Regulador HV SBEC YPG 20A configurado para saída de 6V (motores)
  * Bateria LiPo 5000mAh 3s 11,1V (motores)
* Módulo de hub i2c
* Fita de folha de cobre de 3mm
* Módulo GY-BNO080
* Imãs para a tampa do case de bateria
* Autofalante de 4 Ohm e 3 W

# Software
A programação da ESP32 utiliza a biblioteca chamada PenguinLib disponível na Arduino IDE, também desenvolvida pelo laboratório. Tanto os códigos de calibração de motores, quanto os de utilização do hardware e comando do robô estão disponíveis como exemplos nesta biblioteca.

Na pasta "codes", há dois exemplos de programação da ESP32 (38 pinos). Eles são exemplos em C++ do comando de movimentação da Cherry:
* Dabble: a ESP32 pode se comunicar com o aplicativo Dabble no celular e receber comandos de ação;
* Espaço Inteligente (IS): a ESP32 pode se comunicar com o Espaço Inteligente por MQTT e receber esses mesmos comandos.
