# Criptografia
Implementações realizadas durante a disciplina de Criptografia 

##  Implementando
Em criptografia, um ciframento em blocos trabalha com blocos de comprimento fixo, 
frequentemente de 64 ou 128 bits. Visto que as mensagens podem ter qualquer comprimento,
e dado que criptografar o mesmo texto simples sob a mesma chave sempre produz a mesma saída.

* ECB
O modo mais simples de criptografia é o electronic codebook (ECB). A mensagem é dividida 
em blocos e cada bloco é criptografado separadamente. A desvantagem deste método é que blocos
idênticos de texto plano são criptografados em blocos de texto cifrado idênticos; assim, ele 
também não oculta padrões de dados. No geral, não oferece uma perfeita confidencialidade de 
mensagem, e não é recomendado para uso em protocolos criptográficos em geral.

* CBC
No modo de criptografia CBC (Cypher Block Chaining - Criptografia de Blocos Encadeados),
a cada bloco de texto simples é aplicada uma função XOR junto com o bloco cifrado anterior
antes do texto ser criptografado. Desta forma, cada bloco cifrado fica dependente de todos
os blocos de texto simples processados até este momento. Além disso, para que cada mensagem
seja única, mesmo de um mesmo texto original, um vector de inicialização único deve ser
utilizado no primeiro bloco, preferencialmente gerado aleatoriamente.

* CTR
nova proposta, cada bloco de texto claro é XOR com um contador criptografado. O contador
é incrementado para cada bloco subsequente. Semelhante ao OFB, porém a realimentação é o contador.

