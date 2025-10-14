# 🧠 Projeto Fase 6 – FarmTech Solutions: Visão Computacional com YOLO e CNN

**Autor:** Kleber Foks  
**RM:** 562225  
**Instituição:** FIAP  
**Fase:** 6 – Despertar da rede neural
**Tema:** Sistema de Visão Computacional usando YOLO e CNN  

---

## 📌 Descrição do Projeto

A **FarmTech Solutions** está expandindo seus serviços de Inteligência Artificial para além do agronegócio, incluindo **segurança patrimonial**, **controle de acesso** e **análise de imagens**.

Neste projeto, foi desenvolvido um **sistema de visão computacional** capaz de identificar dois objetos distintos — **teclado (keyboard)** e **mouse** — utilizando a arquitetura **YOLOv8**, além de comparar seus resultados com uma **rede neural convolucional (CNN)** treinada do zero.

---

## ⚙️ Estrutura do Repositório

```
├── data/
│   ├── train/
│   ├── val/
│   ├── test/
│   └── data.yaml
├── runs/
│   ├── tm_e30/
│   ├── tm_e60/
│   └── tm_base/
├── KleberFoks_rm562225_pbl_fase6.ipynb
└── README.md
```

---

## 🚀 Entregas Realizadas

### **Entrega 1 – YOLO Customizado**
- Dataset com **80 imagens** (40 teclado, 40 mouse)
- **Rotulação** via [MakeSense.ai](https://www.makesense.ai)
- Treinamento YOLOv8n com **30 e 60 épocas**
- Comparação entre desempenhos (mAP, precisão, recall, tempo)
- Validação e teste com imagens processadas pelo modelo

### **Entrega 2 – Comparação de Abordagens**
- **YOLOv8s (base)** como rede padrão
- **CNN do zero (PyTorch)** para classificação
- Comparação crítica de precisão, tempo e aplicabilidade

---

## 📊 Resultados Principais

| Modelo | Épocas | Tipo | mAP50-95 | Acurácia | Tempo Treino | Inferência |
|---------|--------|------|-----------|-----------|---------------|-------------|
| YOLOv8n | 30 | Detecção | **0.933** | — | 2.10 min | 0.042 s/img |
| YOLOv8n | 60 | Detecção | **0.945** | — | 1.64 min | 0.026 s/img |
| YOLOv8s | 30 | Detecção | **0.880** | — | 1.25 min | 0.03 s/img |
| CNN | 20 | Classificação | — | **1.000** | 0.35 min | ~0.002 s/img |

📈 **Conclusão:**  
- YOLOv8n (30 épocas) alcançou o melhor equilíbrio entre velocidade e precisão.  
- CNN atingiu acurácia perfeita no dataset pequeno, porém sem detecção espacial.  
- YOLO é mais indicado para **segurança e automação**, pois localiza objetos.  

---

## 🧩 Discussão Técnica

- Dataset pequeno (80 imagens) → risco de **overfitting leve**, mas controlado.  
- YOLO generaliza bem, mesmo com poucas amostras.  
- CNN é excelente para classificação simples, mas não substitui detecção.  
- Ganho de 60 épocas é marginal — 30 já garantem convergência estável.  

---

## 🧠 Tecnologias Utilizadas

- Python 3.12  
- Google Colab  
- Ultralytics YOLOv8  
- PyTorch  
- OpenCV  
- TensorFlow (CNN)  
- MakeSense.ai (rotulação)

---

## 💻 Execução

1. Monte o Google Drive:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
2. Atualize o caminho do dataset:
   ```python
   DATA = "/content/drive/MyDrive/Fase6/data"
   ```
3. Execute o notebook:
   ```
   KleberFoks_rm562225_pbl_fase6.ipynb
   ```
4. O modelo e resultados serão salvos em:
   ```
   /content/drive/MyDrive/Fase6/runs/
   ```

---

## 🎥 Demonstração

📹 **Vídeo (YouTube - Não Listado):**  
👉 [INSIRA O LINK AQUI]

📓 **Notebook no Google Colab:**  
👉 [INSIRA O LINK AQUI]

---

## 🧩 Considerações Finais

O sistema desenvolvido demonstrou a aplicabilidade da visão computacional em cenários reais de automação e segurança, com **alta acurácia e resposta em tempo real**.  
A experiência consolidou o domínio de redes YOLO, CNN e técnicas de treinamento supervisionado.

---

**Autor:** [Kleber Foks](https://github.com/)  
**Data:** Outubro/2025  
**Curso:** Artificial Intelligence & Machine Learning – FIAP
