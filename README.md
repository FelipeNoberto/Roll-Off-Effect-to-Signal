## Sistemas de Comunicação UFCG - Felipe Noberto

### Efeito do Fator de Roll-Off no Sinal

**Descrição e Revisão Teórica**
O sinal QPSK gera um fluxo de bits que é modulado.
O espectro do sinal digital é, em teoria, infinito.
Na prática, os canais de comunicação possuem banda limitada, o que causa "espalhamento" dos pulsos durante a transmissão.
Esse "espalhamento" pode gerar superposição entre pulsos adjacentes, causando a Interferência Entre Símbolos (IES).
A IES, se não for compensada, pode levar a erros na recepção do sinal.
Uma maneira de controlar a IES é formatar os pulsos transmitidos de maneira adequada.
Fator de Roll-Off e Cosseno Levantado

O Cosseno Levantado é uma técnica de formatação de pulsos que, em conjunto com a taxa de amostragem adequada, pode eliminar a IES.

Na prática, a implementação ideal do filtro formatador de pulsos é difícil, pois:

O filtro ideal não é fisicamente realizável.
A forma de onda depende da precisão dos relógios da recepção, o que pode resultar em alta IES.
Solução com Fator de Roll-Off

Existe um conjunto de filtros com diferentes fatores de Roll-off que atendem às necessidades de comunicação. O fator de Roll-off (α) é definido por:

α = 1 - (f1/B0)

Onde:

α: Fator de Roll-off
f1: Frequência de corte do filtro
B0: Largura de banda de Nyquist
O valor de α varia entre 0 e 1, sendo 0 o valor mais próximo do filtro ideal (f1 = B0).

A largura de banda de transmissão necessária (B) usando o cosseno levantado é dada por:

B = B0(1 + α)

Onde:

B: Largura de banda de transmissão
B0: Largura de banda de Nyquist
α: Fator de Roll-off
Consequências do Fator de Roll-Off

O uso do cosseno levantado aumenta a largura de banda de transmissão em relação à solução ideal (Nyquist) em αB0. A razão entre o excesso de banda e a banda de Nyquist é igual a α.

O fator de Roll-off é um parâmetro crucial para controlar a banda de frequência utilizada na comunicação digital. Ao escolher o valor ideal de α, podemos otimizar o uso do espectro de frequência, minimizando a interferência entre símbolos e garantindo a qualidade da comunicação.
