
# mikroti_automacoes
Para executar este script, basta copiar tudo o que esta acima, e colar direto no terminal
1

Deve ser seguida a ordem de acordo com a interface, ou seja, no exemplo abaixo, temos que o Link da

Ether1 --> 10Mbps

Ether2 --> 20Mbps

Ether3 --> 30Mbps

#Exemplos:

# 1-Criando o PCC com 3 Interfaces de chegada do Link, e com a capacidade de cada uma delas

$balance interfaces="ether1,ether2,ether3" cargas="10,20,30"

# Para adicionar mais interfaces, basta colocar uma virgula, e o nome correto da interface, e também acrescentar o numero correspondente ao trafego do Link que chega por essa interface.

Exemplo:

$balance interfaces="ether1,ether2,ether3,ether4" cargas="10,20,30,40"

$balance interfaces="ether1,ether2,ether3,ether4,ether5" cargas="10,20,30,40,50"

......

#Para remover as regras criadas, basta executar tudo da forma que está acima, informando o parametro "acao" com opção de remover

Exemplo

$balance acao=remover

#Ou então executar as seguintes regras direto no console do mikrotik

/ip route remove [find where comment="AUTOMACAO PCC SCRITP" ]

/ip firewall mangle remove [find where comment="AUTOMACAO PCC SCRITP" ]
