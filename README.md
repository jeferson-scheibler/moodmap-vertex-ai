# 🌍 MoodMap – Reconhecimento Emocional com Vertex AI

O **MoodMap** é um projeto Android que combina **Machine Learning**, **Visão Computacional** e **Google Vertex AI** para identificar emoções humanas por meio da câmera do celular. A ideia é detectar expressões faciais em tempo real, enviar os dados para um modelo treinado no Vertex AI e exibir a emoção detectada no app.

Acesse a Wiki para:

- Entender o propósito do projeto
- Ver como o modelo foi treinado no Vertex AI
- Aprender a usar o ML Kit para detecção facial
- Conectar seu app Android ao endpoint do Vertex AI
- Gerar dados sintéticos para treinar modelos de reconhecimento de emoções

## 📖 Wiki Oficial do Projeto

Para facilitar o entendimento e a replicação deste experimento, criamos uma Wiki estruturada com um **guia completo passo a passo**.

### 🧭 Estrutura da Wiki

A Wiki está organizada em tópicos sequenciais:

1. **Home** - https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki
   - Visão geral do projeto, propósito e funcionamento.
   
3. **Sobre o Vertex AI** - https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki/Sobre-o-Vertex-AI
   - Introdução ao Vertex AI e seu papel no projeto.
   
5. **Reconhecimento de Emoções Faciais com ML Kit** - https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki/Reconhecimento-de-Emo%C3%A7%C3%B5es-Faciais-com-ML-Kit
   - Explicação sobre os atributos faciais analisados e como o dataset foi construído.

7. **Treinamento do Modelo** - https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki/Treinamento-do-Modelo
   - Passo a passo para importar o CSV, treinar o modelo no Vertex AI e ativar o endpoint.

8. **App Android com Vertex AI ML Kit** - https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki/App-Android-com-Vertex-AI-ML-Kit
   - Guia prático de como criar o app, configurar câmera, capturar dados, analisar emoções e integrar com o Vertex AI.

---

## 🚀 Requisitos Básicos

- Conta Google Cloud com faturamento ativado
- Projeto criado no GCP
- Permissões para criar endpoints no Vertex AI
- Android Studio instalado
- Dispositivo com câmera frontal ou emulador com suporte

---

## 📂 Estrutura deste repositório

| Arquivo | Descrição |
|--------|-----------|
| `Gerar_Valores_de_Emoções_para_Análise_Facial.ipynb` | Notebook para gerar dados sintéticos de emoções |
| `gerar_valores_de_emoções_para_análise_facial.py` | Versão Python do script de geração de dados |
| `LICENSE` | Licença do projeto |
| `README.md` | Este arquivo de apresentação |

---

📌 Se você está buscando uma forma prática de usar **ML Kit + Vertex AI** em projetos Android com reconhecimento facial, o **MoodMap** é o ponto de partida ideal.

---

## 🤝 Contribuições

Sinta-se à vontade para abrir issues ou enviar PRs para melhorias!

---

## 📬 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais detalhes.
