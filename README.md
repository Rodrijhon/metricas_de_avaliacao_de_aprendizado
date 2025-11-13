# metricas_de_avalia-o_de_aprendizad
Cálculo de Métricas de Avaliação
Descrição do Projeto

Este projeto tem como objetivo calcular as principais métricas utilizadas para avaliar modelos de classificação em Machine Learning.
As métricas calculadas são:

Acurácia

Sensibilidade (Recall)

Especificidade

Precisão

F1-Score

Essas métricas são obtidas a partir dos valores da Matriz de Confusão, composta por:

VP – Verdadeiros Positivos

VN – Verdadeiros Negativos

FP – Falsos Positivos

FN – Falsos Negativos

No projeto, você pode escolher livremente os valores da matriz de confusão, pois o objetivo é aprender a calcular cada métrica.

🧑‍💻 1. Como executar o projeto no Google Colab
✔ Passo 1 — Acesse o Google Colab

Abra o link: https://colab.research.google.com/

✔ Passo 2 — Crie um novo notebook

Clique em File → New Notebook (Arquivo → Novo Notebook)

✔ Passo 3 — Copie o código abaixo para uma célula
# Projeto Final - Módulo 4
# Cálculo das principais métricas de avaliação

# Definindo uma matriz de confusão arbitrária
# Você pode mudar os valores!
VP = 50   # Verdadeiros Positivos
VN = 40   # Verdadeiros Negativos
FP = 10   # Falsos Positivos
FN = 5    # Falsos Negativos

print("=== MATRIZ DE CONFUSÃO ESCOLHIDA ===")
print(f"VP = {VP}, VN = {VN}, FP = {FP}, FN = {FN}\n")

# -----------------------------
# Cálculo das métricas
# -----------------------------

# Acurácia
acuracia = (VP + VN) / (VP + VN + FP + FN)

# Sensibilidade (Recall)
sensibilidade = VP / (VP + FN)

# Especificidade
especificidade = VN / (VN + FP)

# Precisão
precisao = VP / (VP + FP)

# F-score (F1-score)
f1_score = 2 * (precisao * sensibilidade) / (precisao + sensibilidade)


# -----------------------------
# Exibindo os resultados
# -----------------------------
print("=== RESULTADOS DAS MÉTRICAS ===")
print(f"Acurácia:        {acuracia:.4f}")
print(f"Sensibilidade:   {sensibilidade:.4f}")
print(f"Especificidade:  {especificidade:.4f}")
print(f"Precisão:        {precisao:.4f}")
print(f"F1-Score:        {f1_score:.4f}")

# Explicação automática
print("\n=== INTERPRETAÇÃO DAS MÉTRICAS ===")
print("✔ Acurácia: proporção total de acertos do modelo.")
print("✔ Sensibilidade: capacidade de identificar corretamente os positivos.")
print("✔ Especificidade: capacidade de identificar corretamente os negativos.")
print("✔ Precisão: quanto das previsões positivas realmente são positivas.")
print("✔ F1-Score: média harmônica entre precisão e sensibilidade.\n")

✔ Passo 4 — Execute o código

Pressione Shift + Enter para rodar a célula.

2. Fórmulas utilizadas
Métrica	Fórmula
Acurácia	(VP + VN) / (VP + VN + FP + FN)
Sensibilidade (Recall)	VP / (VP + FN)
Especificidade	VN / (VN + FP)
Precisão (Precision)	VP / (VP + FP)
F1-Score	2 × (Precisão × Recall) / (Precisão + Recall)

3. Explicação das métricas

Acurácia

Indica o percentual total de acertos do modelo.
Mostra quantas classificações foram feitas corretamente.

Sensibilidade (Recall)

Mostra o quanto o modelo consegue identificar corretamente os casos positivos.
Importante para detectar doenças, fraudes, etc.

Especificidade

Mostra o quanto o modelo consegue identificar corretamente os casos negativos.
Útil para evitar falsos alarmes.

Precisão

Entre os elementos que o modelo classificou como positivos, quantos realmente são positivos.

F1-Score

Combina Precisão e Recall em uma única métrica equilibrada.

4. Como alterar a matriz de confusão

No início do código, modifique os valores como quiser:

VP = 30
VN = 70
FP = 5
FN = 15


O código recalculará automaticamente todas as métricas.

Autor : Jhon Rodrigues
Novembro 2025
