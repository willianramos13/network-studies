**BGP (Border Gateway Protocol)**

O Border Gateway Protocol (BGP) é o protocolo de roteamento utilizado para trocar informações entre Sistemas Autônomos (Autonomous Systems - AS). Diferente dos protocolos IGP, como OSPF e RIP, que atuam dentro de uma única organização, o BGP foi desenvolvido para conectar diferentes redes, sendo a base do roteamento da Internet.

Neste diretório serão documentados os laboratórios desenvolvidos durante meus estudos de BGP utilizando MikroTik CHR (RouterOS v7). O objetivo não é apenas demonstrar comandos de configuração, mas compreender o funcionamento do protocolo, seus atributos, o processo de seleção de rotas e as boas práticas utilizadas por provedores de Internet (ISP).

Ao longo dos laboratórios serão abordados temas como:

Formação de sessões eBGP
Troca de prefixos entre Sistemas Autônomos
Seleção do melhor caminho
AS-PATH
AS-PATH Prepend
Local Preference
MED
Communities
Engenharia de tráfego
Cenários práticos de ISP

Inicialmente, os laboratórios serão desenvolvidos utilizando MikroTik CHR, permitindo o aprendizado dos conceitos fundamentais do protocolo, análise do comportamento das rotas e validação prática de cada configuração em um ambiente controlado.

À medida que os estudos evoluírem para cenários mais próximos de ambientes de produção e provedores de Internet (ISP), poderão ser incorporados equipamentos e laboratórios utilizando Cisco, possibilitando comparar implementações, comandos e boas práticas entre diferentes fabricantes.

Todo o ambiente é construído em laboratório, permitindo validar cada conceito por meio de testes práticos, análise das tabelas de roteamento e observação do comportamento do protocolo diante de diferentes cenários.
