**Objetivo**

Compreender o funcionamento dos protocolos ARP (Address Resolution Protocol) e ICMP (Internet Control Message Protocol) através de testes práticos em ambiente GNS3 utilizando roteadores Mikrotik.

**Topologia**

MK01                          MK02                          MK03
10.0.0.1/24 -------- 10.0.0.2/24 | 10.0.0.5/24 -------- 10.0.0.6/24

**Endereçamento**

Equipamento	Interface	Endereço IP

MK01	ether1	10.0.0.1/24
MK02	ether1	10.0.0.2/24
MK02	ether2	10.0.0.5/24
MK03	ether1	10.0.0.6/24

**Objetivos dos testes**

Validar a comunicação entre MK01 e MK02.
Validar a comunicação entre MK02 e MK03.
Observar a criação de entradas ARP.
Capturar pacotes ARP e ICMP no Wireshark.
Entender a diferença entre comunicação local e comunicação roteada.

**Teste  - ARP entre MK01 e MK02**

Antes do ping:

/ip arp print

Realizar o teste:

ping 10.0.0.2

**Resultado esperado:**

Geração de ARP Request.
Recebimento de ARP Reply.
Criação de entrada dinâmica na tabela ARP.

**Adicionar rotas estáticas:**

MK01
/ip route add dst-address=10.0.0.0/24 gateway=10.0.0.2

MK03
/ip route add dst-address=10.0.0.0/24 gateway=10.0.0.5

**Realizar o teste:**

ping 10.0.0.6

**Aprendizados**

O ARP funciona apenas dentro do segmento local.
Roteadores não encaminham broadcasts ARP.
Para alcançar redes remotas, o host resolve apenas o MAC do gateway.
O protocolo ICMP é utilizado para validar conectividade através do comando ping.
O Wireshark permite visualizar toda a sequência de ARP Request, ARP Reply, ICMP Echo Request e ICMP Echo Reply.

**Conclusão:**

O laboratório demonstrou a relação entre ARP e ICMP em redes locais e roteadas. Foi possível observar que a resolução ARP ocorre apenas para dispositivos presentes no mesmo segmento de rede, enquanto a comunicação com redes remotas depende do roteamento através do gateway.


