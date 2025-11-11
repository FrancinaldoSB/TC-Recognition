# 📱 TC-Recognition: Comparativo de Classificação em Reconhecimento de Atividades Humanas (HAR)

📜 **Licença:** MIT  
🐍 **Requisitos:** Python 3.8+  
📦 **Principais dependências:** `scikit-learn`  
📊 **Base de dados:** [UCI HAR Dataset](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones)

## 🧠 Visão Geral

Este projeto implementa um **estudo comparativo** entre três classificadores — **KNN**, **SVM** e **MLP** — aplicados ao problema de **Reconhecimento de Atividades Humanas (HAR)**.

O dataset utilizado contém **dados de sensores inerciais de smartphones** (acelerômetro e giroscópio), provenientes do **UCI HAR Dataset**, amplamente usado em pesquisas de aprendizado de máquina.

O estudo foi conduzido em **dois cenários experimentais**:

1. 🔹 **Sem LDA** → Dados originais normalizados (561 atributos)  
2. 🔸 **Com LDA** → Redução supervisionada para **5 componentes** (100% da variância explicada)

## ⚙️ Metodologia

O pipeline de experimentação seguiu as seguintes etapas:

1. **Carregamento** dos dados brutos do UCI HAR  
2. **Normalização** dos atributos com `StandardScaler`  
3. **Aplicação opcional** da análise discriminante linear (**LDA**)  
4. **Treinamento** e **validação cruzada** dos modelos:
   - SVM com kernel RBF  
   - MLP (rede neural multicamadas)  
   - KNN com `k=5`
5. **Avaliação de desempenho** com métricas de acurácia média e desvio padrão

## 📈 Resultados

| Modelo       | Sem LDA                | Com LDA                |
|---------------|------------------------|------------------------|
| 🧮 **SVM (RBF)** | **98,58% (±0,24%)**     | **97,93% (±0,27%)**     |
| 🧠 **MLP**       | **98,41% (±0,46%)**     | **96,63% (±0,19%)**     |
| 📏 **KNN (k=5)** | **96,31% (±0,54%)**     | **97,90% (±0,37%)**     |


## 👥 Autores

**Iago Roberto¹**  
**Francinaldo Barbosa¹**  

¹ *Universidade Federal do Piauí – Campus Senador Helvídio Nunes Barros (UFPI)*  
📬 Caixa Postal 64049-55 – 64.607-670 – Picos – PI – Brasil  
📧 Emails: `{iago.almeida, francinaldo.barbosa}@ufpi.edu.br`

## 💡 Licença

Este projeto está licenciado sob a **Licença MIT**.  
Sinta-se livre para usar, modificar e distribuir este código.
