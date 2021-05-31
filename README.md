########################################################################################################################################################

				    REDES

########################################################################################################################################################

			CONCEITOS BÁSICOS DE REDE

	Comunicação de dados é a troca de informação entre dois dispositivos através de algm meio de comunicação como, por exemplo, um par e fios. 
Um distema básico de comunicação de dados é composto por conco elementos:

	São eles:
	     Mensagem | Transmissor | Receptor | Meio | Protocolo]


Mensagem: É a informação a ser transmitida

Transmissor: É o dispositivo que envia a mensagem

Receptor: É o dispositivo que rece a mensagem

Meio: É o caminho físico por onde trafega

Protocolo: É o conjunto de regras que rege a comunicação de dados.



~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

		Emissor                             Receptor
  		  |                Meio                |
  		   ____________________________________
	
			          Mensagem


======================== CLASSIFICAÇÃO DAS REDES ===========================

Uma das características mais utilizadas para a classificação das redes é a sua abrangência geográfica. Assim, é convencionada a seguinte classificação:

1 - LAN's (Local Area Networks) -Redes locais.
2 - MAN's (Metopolitan Area Networks) - Metropolitanas.
3 - WAN's (Wide Area Networks) - Geograficamente distribuídas.





============================== TOPOLOGIAS ==================================

Barramento
Estrela
Anel


BARRAMENTO

	Rede em barramento é uma topologia de rede em que todos os computadores estão ligados por vários cabos em vários barramentos físico de dados.
Apesar de os dados não passarem por dentro de cada um dos nós, apenas uma máquina pode “escrever” no barramento num dado momento. Todas as outras “escutam” e recolhem para si os dados destinados a elas. Quando um computador estiver a transmitir um sinal, toda a rede fica ocupada e se outro computador tentar enviar outro sinal ao mesmo tempo, ocorre uma colisão e é preciso reiniciar a transmissão

ESTRELA

	Na topologia de rede em estrela, toda a informação deve passar obrigatoriamente por uma estação central inteligente, que deve conectar cada estação da rede e distribuir o tráfego para que uma estação não receba, indevidamente, dados destinados às outras. 

A topologia em estrela é caracterizada por um elemento central que "gerencia" o fluxo de dados da rede, estando diretamente conectado (ponto-a-ponto) a cada nó, daí surgiu a designação "Estrela". As informações trafegam na rede de um host para o outro. Toda informação enviada de um nó para outro é enviada primeiro ao dispositivo que fica no centro da estrela, portanto os dados não passam por todos os hosts. O concentrador encarrega-se de encaminhar o sinal especificamente para as estações solicitadas, economizando tempo. 

As redes em estrela, que são as mais comuns hoje em dia, utilizam cabos de par trançado e uma switch como ponto central da rede. 

ANEL

	A topologia de rede em anel consiste em estações conectadas através de um circuito fechado, em série. O anel não interliga as estações diretamente, mas consiste de uma série de repetidores ligados por um meio físico, sendo cada estação ligada a estes repetidores. É uma configuração em desuso.

Nesta topologia cada estação está conectada a apenas duas outras estações, quando todas estão ativas. Uma desvantagem é que se, por acaso apenas uma das máquinas falhar, toda a rede pode ser comprometida, já que a informação só trafega em uma direção, que no caso é CIRCULAR.
========================================================================================================================================================

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ MEIOS DE TRANSMISSÃO ~~~~~~~~~~~~~~~~~~~~~~~~
ESCREVER DEPOIS SOBRE OS TIPOS DE CABOS

============================================================================
########################################################################################################################################################

****************************** MODELO OSI **********************************

MODELO OSI (Open System Interconnection)

	Este modelo é dividido em sete camadas hierárquicas, ou seja, cada camada usa as funções da própria ou da camada anterior, para esconder a complexidade e transparecer de modo simples as operações ao usuário, seja ele um programa ou uma outra camada.



As camadas são empilhadas na seguinte ordem:

	7. Camada de aplicação;
	6. Camada de apresentação;
	5. Camada de sessão;
	4. Camada de transporte;
	3. Camada de rede;
	2. Camada de enlace de dados;
	1. Camada física.


1 - CAMADA FÍSICA

	A camada física é responsável por definir se a transmissão pode ser ou não realizada nos dois sentidos simultaneamente. Sendo a camada mais baixa do modelo OSI, diz respeito a transmissão e recepção do fluxo de bits brutos não-estruturados em um meio físico. Ela descreve as interfaces elétricas, ópticas, mecânicas e funcionais para o meio físico e transporta sinais para todas as camadas superiores.

2 - CAMADA DE ENLACE DE DADOS

	A camada de enlace ou link de dados. 
Esta camada detecta e, opcionalmente, corrige erros que possam acontecer no nível físico. É responsável por controlar o fluxo (recepção, delimitação e transmissão de quadros) e também estabelece um protocolo de comunicação entre sistemas diretamente conectados.

3 - CAMADA DE REDE

	A camada de rede realiza roteamento de funções, e também pode realizar a fragmentação e remontagem e os erros de entrega de relatório. Roteadores operam nesta camada, enviando dados em toda a rede estendida e tornando a Internet possível. Este é um esquema de endereçamento lógico - os valores são escolhidos pelo engenheiro de rede. O esquema de endereçamento não é hierárquico.

A camada de rede pode ser dividida em três subcamadas:

	º Sub-rede de acesso - considera protocolos que lidam com a interface para redes, tais como X.25;
	º Sub-rede dependente de convergência - necessária para elevar o nível de uma rede de trânsito, até ao nível de redes em cada lado;
	º Sub-rede independente de convergência - lida com a transferência através de múltiplas redes. Controla a operação da sub rede roteamento de pacotes, controle de congestionamento, tarifação e permite que redes heterogêneas sejam interconectadas.

4 - CAMADA DE TRANSPORTE

	A camada de transporte é responsável por receber os dados enviados pela camada de sessão e segmentá-los para que sejam enviados a camada de rede, que por sua vez, transforma esses segmentos em pacotes. No receptor, a camada de Transporte realiza o processo inverso, ou seja, recebe os pacotes da camada de rede e junta os segmentos para enviar à camada de sessão.

Isso inclui controle de fluxo, ordenação dos pacotes e a correção de erros, tipicamente enviando para o transmissor uma informação de recebimento, garantindo que as mensagens sejam entregues sem erros na sequência, sem perdas e duplicações.

bjetivo final da camada de transporte é proporcionar serviço eficiente, confiável e de baixo custo. O hardware e/ou software dentro da camada de transporte e que faz o serviço é denominado entidade de transporte.

5 - CAMADA DE SESSÃO
	
	Responsável pela troca de dados e a comunicação entre hosts, a camada de Sessão permite que duas aplicações em computadores diferentes estabeleçam uma comunicação, definindo como será feita a transmissão de dados, pondo marcações nos dados que serão transmitidos. Se porventura a rede falhar, os computadores reiniciam a transmissão dos dados a partir da última marcação recebida pelo computador receptor.

6 - CAMADA DE APRESENTAÇÃO

	A camada de Apresentação, também chamada camada de Tradução, converte o formato do dado recebido pela camada de Aplicação em um formato comum a ser usado na transmissão desse dado, ou seja, um formato entendido pelo protocolo usado. Um exemplo comum é a conversão do padrão de caracteres (código de página) quando o dispositivo transmissor usa um padrão diferente do ASCII. Pode ter outros usos, como compressão de dados e criptografia.

Os dados recebidos da camada 7 estão descomprimidos, e a camada 6 do dispositivo transmissor fica responsável por comprimir esses dados. A transmissão dos dados torna-se mais rápida, já que haverá menos dados a serem transmitidos: os dados recebidos da camada 4 foram "encolhidos" e enviados à camada 1.

Para aumentar a segurança, pode-se usar algum esquema de criptografia neste nível, sendo que os dados só serão descodificados na camada 6 do dispositivo receptor.

Ela trabalha transformando os dados em um formato no qual a camada de aplicação possa aceitar, minimizando todo tipo de interferência.

7 - CAMADA DE APLICAÇÃO

	A camada de aplicação corresponde às aplicações (programas) no topo da camada OSI que serão utilizadas para promover uma interação entre a máquina-usuário (máquina destinatária e o usuário da aplicação). Esta camada também disponibiliza os recursos (protocolo) para que tal comunicação aconteça, por exemplo, ao solicitar a recepção de e-mail através do aplicativo de e-mail, este entrará em contato com a camada de Aplicação do protocolo de rede efetuando tal solicitação (POP3 ou IMAP).

Tudo nesta camada é relacionado ao software. Alguns protocolos utilizados nesta camada são: HTTP, SMTP, FTP, Telnet, SIP, RDP, IRC, SNMP, NNTP, POP3, IMAP, BitTorrent, DNS, ICMP.




########################################################################################################################################################



Protocolo TCP/IP -- Protocolo usado na internet e nas redes locais nos computadores

IP -- Internet Protocol -- Define uma indentidade, uma identificação para cada dispositivo da rede.
É um numero que deve ser único, só uma maquina só um dispositivo pode ter esse numéro

	Esse numéro é composto por 32 bits, 32 posições que podem variar de 0 e 1 o equivalente a 4 bilhões de combinações, recentemente esse quantidade de possibilidades foi esgotada isso acontece pois essa é a versão 4( IPV4)
	Já existe uma nova versão a IPV6 que aumenta muita essa possibilidade de combinações, mas mesmo assim o IPV4 ainda é muito utilizado


Para facilitar os 32 bits foram divididos em quatro grupos de 8 bits, que são chamados de octetos

00000000 | 00000000 | 00000000 | 00000000
   0/255     0/255      0/255	   0/255

cada octeto podem ter 256 possibilidades de combinações que são enumerados do 0 ao 255


########################################################################################################################################################
			      CLASSES DE IP


A - 10.0.0.1 -> 10.255.255.255
B - 172.16.0.0 -> 172.31.255.255
C - 192.168.0.0 -> 192.168.255.255


Obs. classe a,b e c reservado para redes internas
