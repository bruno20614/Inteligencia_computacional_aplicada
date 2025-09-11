1. O que implementar
(A) Perceptron Binário (forma homogênea)

Perceptron clássico: 
x~=[x;1]
x
~
=[x;1], 
w~=[w;b]
w
~
=[w;b], escore 
z=w~⊤x~
z=
w
~
⊤
x
~
, margem 
u=yz
u=yz.

Margem fixa: atualizar se 
u≤τ
u≤τ.

Passo agressivo: 
η\*=τ−u∥x~∥2
η
\*
=
∥
x
~
∥
2
τ−u
	​

.

Averaged Perceptron: média temporal dos pesos.

Voted Perceptron: voto com contagens.

Pocket: mantém melhor 
w\*
w
\*
.

Weight decay (L2).

Early stopping: com paciência usando validação.

(B) Multiclasse

One-vs-Rest (OvR): um binário por classe.

Crammer–Singer (direto): matriz 
W
W, atualização em 
y
y e 
y^
y
^
	​

.

(Opcional) margem multiclasses com hinge.

2. O que avaliar

Métricas: acurácia, macro-F1 (binário → também AUC).

Margens: distribuição das margens com e sem margem fixa/agressiva.

Calibração: Brier score, ECE (com ou sem Platt scaling).

Eficiência: tempo vs. número de amostras/dimensões (log–log).

Robustez: efeito de ruído nos rótulos (5%).

Sensibilidade: varrer 
η,τ,λ
η,τ,λ.

3. O que entregar

Notebook no Colab:

Do zero, reprodutível, modular (classes/funções).

Testes rápidos (doctests/asserts).

Sementes fixas.

Compartilhar com o professor como editor.

Relatório (6–9 páginas, PDF):

Metodologia.

Experimentos.

Tabelas/figuras.

Análises.

Ablation study e estudo de sensibilidade.

Apêndice:

Fórmulas (margens, passo agressivo, ECE, Brier).

Esboço do Teorema de Novikoff.

Análise de complexidade (teórica + empírica).

4. Experimentos obrigatórios

Comparações:

Clássico × Margem fixa × Passo agressivo.

Averaged × Voted × Pocket.

OvR × Crammer–Singer (tempo/época + acurácia).

Sensibilidade a hiperparâmetros.

Complexidade: gráficos log–log tempo × 
n
n e × 
d
d.

Calibração: reliability diagrams, ECE, Brier.

Intervalo de confiança: bootstrap para macro-F1.

5. Bases de dados obrigatórias

Binário: Breast Cancer ou USPS (precisa macro-F1 ≥ 0,95 ou AUC ≥ 0,98).

Multiclasse: MNIST ou Statlog (precisa ≥ 90% de acurácia).

Outros: USPS completo e 20 Newsgroups (opcional reforço).

6. Restrições

Proibido: scikit-learn, statsmodels, bibliotecas prontas de ML, faiss, annoy, hnswlib.

Permitido: numpy, pandas, matplotlib, scipy.io, numba (opcional).

Pré-processamento só com dados de treino na validação cruzada.