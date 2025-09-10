Ao final, o(a) aluno(a) deverá ser capaz de: (i) implementar do zero o perceptron biná-
rio em forma homogênea, incluindo margem fixa e passo agressivo; (ii) implementar

Averaged e Voted Perceptron, Pocket, weight decay e early stopping; (iii) estender
para multiclasse via One-vs-Rest e direto (Crammer–Singer); (iv) avaliar margens,
calibração (ECE/Brier) e complexidade.

1. Perceptron básico

Objetivo: Implementar o perceptron binário simples (forma homogênea, sem viés separado).

Etapas:

Representar os dados na forma homogênea (adicionar dimensão +1 para o bias).

Implementar a regra de atualização clássica.

Garantir que o algoritmo funciona em um dataset simples (ex.: AND, OR, toy datasets do sklearn).

2. Extensões do perceptron binário

Aqui você adiciona as variações pedidas:

Margem fixa: atualizar os pesos não apenas quando erra, mas também quando a margem é violada.

Passo agressivo: calcular passo de atualização de forma adaptativa (depende do erro).

Pocket algorithm: manter a melhor solução encontrada até agora.

Weight decay: regularização multiplicando pesos por fator < 1 a cada iteração.

Early stopping: parar quando a melhora no erro de validação estabiliza.

3. Variações de ensemble

Averaged Perceptron: manter média dos pesos ao longo das iterações.

Voted Perceptron: armazenar cada vetor de pesos com um peso de votação proporcional ao tempo de uso.

Esses dois se encaixam bem depois das extensões do passo 2.

4. Multiclasse

One-vs-Rest (OvR): treinar um perceptron binário para cada classe (vs todas as outras).

Crammer–Singer: implementar o perceptron multiclasse direto (atualiza pesos entre classe correta e predita).

5. Avaliação

Margens: medir margens obtidas pelas classificações.

Calibração: avaliar com métricas como ECE (Expected Calibration Error) e Brier Score.

Complexidade: analisar custo computacional dos diferentes algoritmos (tempo, memória).


