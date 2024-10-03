Projeto: Sistema de Contagem Regressiva com Desarme de Bomba
Descrição do Projeto
Este projeto consiste em um sistema de contagem regressiva que simula a desativação de uma bomba. Utilizando um teclado matricial para inserir a senha e um display OLED para exibir mensagens e a contagem, o sistema oferece feedback sonoro através de um buzzer. O projeto é ideal para fins educacionais e para entender como trabalhar com microcontroladores, displays e interação do usuário.

Materiais Necessários
Para a construção deste projeto, você precisará dos seguintes componentes:

Microcontrolador:

Arduino Uno ou qualquer placa compatível.
Displays:

1x Display OLED (SSD1306).
1x Display de 7 segmentos (TM1637).
Teclado:

1x Teclado matricial 4x4.
Buzzer:

1x Buzzer piezoelétrico.
Fios de Conexão:

Jumper wires para realizar as conexões.
Protoboard:

Para montagem do circuito.
Esquema de Conexão
Display OLED:

Conecte os pinos SDA e SCL do OLED aos pinos A4 e A5 do Arduino, respectivamente.
Display TM1637:

Conecte o pino CLK ao pino A2 e o pino DIO ao pino A3 do Arduino.
Teclado Matricial:

Conecte as linhas (ROWS) aos pinos 9, 8, 7 e 6 do Arduino.
Conecte as colunas (COLS) aos pinos 5, 4, 3 e 2 do Arduino.
Buzzer:

Conecte o pino positivo do buzzer ao pino 11 do Arduino e o pino negativo ao GND.
Funcionamento do Código
O código foi estruturado para gerenciar a contagem regressiva, a entrada do usuário através do teclado matricial e a exibição de mensagens em dois displays diferentes. A seguir, um resumo das principais funções e características do código:

Bibliotecas Utilizadas:

Wire: Para comunicação I2C com o display OLED.
Adafruit_GFX e Adafruit_SSD1306: Para controlar o display OLED.
TM1637Display: Para manipular o display de 7 segmentos.
Keypad: Para capturar as entradas do teclado matricial.
Definições Iniciais:

São definidas constantes para os pinos dos componentes e variáveis para controle do tempo e estado do sistema (como paused e bombaDesarmada).
Configuração Inicial (setup):

Inicializa os displays e configura os pinos.
Verifica se o display OLED está funcionando corretamente.
Limpa a tela do OLED.
Atualização do Display (updateDisplay):

Converte o tempo restante em segundos e milissegundos.
Alterna a exibição de dois pontos a cada 500 ms.
Manipulação da Entrada do Teclado (handleKeypress):

Lê a entrada do usuário.
Se a tecla # for pressionada, verifica se a senha está correta. Se sim, desarma a bomba; se não, reinicia o contador ou zera o tempo após tentativas incorretas.
Atualização do Buzzer (updateBuzzer):

Modula o som do buzzer conforme o tempo restante.
Loop Principal (loop):

Verifica o estado do temporizador e atualiza a contagem.
Exibe a mensagem "KABUM! GAME OVER" quando o tempo acaba.
Se a bomba estiver desarmada, exibe a mensagem "BOMBA DESARMADA".
Conclusão
Esse projeto oferece uma excelente oportunidade para aprender sobre componentes eletrônicos e programação em Arduino. Você pode expandir esse projeto adicionando mais funcionalidades, como uma sequência de desarmamento mais complexa, ou integrando sensores para detecção de movimento. Experimente e divirta-se enquanto aprende!




