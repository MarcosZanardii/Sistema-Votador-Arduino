Sistema de Votação com LEDs
Este projeto implementa um sistema de votação simples utilizando chaves (botões) e LEDs, desenvolvido para a plataforma Arduino. O sistema permite que até três pessoas votem "SIM" ou "NÃO", com os resultados sendo exibidos através de LEDs.

Componentes
Chaves (Inputs):

CHAVE1: Botão para a primeira pessoa votar.
CHAVE2: Botão para a segunda pessoa votar.
CHAVE3: Botão para a terceira pessoa votar.
LEDs (Outputs):

LED_SIM: Acende se houver pelo menos duas votações "SIM".
LED_NAO: Acende se houver pelo menos uma votação "NÃO" sem unanimidade.
LED_USIM: Acende se houver unanimidade em "SIM".
LED_UNAO: Acende se houver unanimidade em "NÃO".
Funcionamento
Configuração:

Os pinos das chaves são configurados como entradas, enquanto os pinos dos LEDs são configurados como saídas no método setup().
Processo de Votação:

As votações das chaves são lidas continuamente no loop principal (loop()).
O sistema determina os resultados e acende os LEDs apropriados com base nas votações:
Maioria "SIM": O LED "SIM" acende se pelo menos duas chaves estiverem em "HIGH".
Unanimidade "SIM": O LED "USIM" acende se todas as chaves estiverem em "HIGH".
Unanimidade "NÃO": O LED "UNAO" acende se todas as chaves estiverem em "LOW".
Maioria "NÃO": O LED "NAO" acende se houver pelo menos uma votação "LOW" sem unanimidade.
Desligamento dos LEDs:

A função desligaLed() é utilizada para desligar os LEDs que não representam o resultado atual da votação, garantindo que apenas um LED esteja aceso de cada vez.
Como Usar
Materiais Necessários:

Placa Arduino (por exemplo, Arduino Uno).
3 Botões (ou chaves).
4 LEDs (vermelho, verde ou outras cores conforme preferência).
Resistores (220Ω para LEDs).
Fios de conexão.
Protoboard (opcional).
Montagem:

Conecte os botões aos pinos CHAVE1, CHAVE2, CHAVE3 do Arduino.
Conecte os LEDs aos pinos LED_SIM, LED_NAO, LED_USIM, LED_UNAO e aos resistores.
Programação:

Carregue o código fornecido neste repositório para a sua placa Arduino usando a IDE do Arduino.
Testes:

Pressione os botões para registrar as votações e observe quais LEDs acendem conforme as regras de votação.
Conclusão
Este sistema de votação é uma maneira divertida e educativa de entender lógica de controle e programação com Arduino. Você pode expandir este projeto adicionando mais funcionalidades, como um contador de votos ou um display para mostrar os resultados.

Licença
Este projeto está sob a licença MIT. Sinta-se à vontade para modificar e distribuir conforme necessário.
