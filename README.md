# 🌍 MoodMap – Reconhecimento Emocional com Vertex AI

O **MoodMap** é um projeto Android que combina **Machine Learning**, **Visão Computacional** e **Google Vertex AI** para identificar emoções humanas por meio da câmera do celular. A ideia é detectar expressões faciais em tempo real, enviar os dados para um modelo treinado no Vertex AI e exibir a emoção detectada no app.

Este repositório contém:
- Código-fonte Android do app (no Wiki)
- Scripts de geração de dados
- Treinamento e deploy de modelo no Vertex AI (no Wiki)

## 📖 Wiki Oficial do Projeto

Para facilitar o entendimento e a replicação deste experimento, criamos uma Wiki estruturada com um **guia completo passo a passo**.

### 🧭 Estrutura da Wiki

A Wiki está organizada em tópicos sequenciais:

1. **Home**
   https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki
   Visão geral do projeto, propósito e funcionamento.

2. **Sobre o Vertex AI**
   https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki/Sobre-o-Vertex-AI
   Introdução ao Vertex AI e seu papel no projeto.

3. **Reconhecimento de Emoções Faciais com ML Kit**
   https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki/Reconhecimento-de-Emo%C3%A7%C3%B5es-Faciais-com-ML-Kit
   Explicação sobre os atributos faciais analisados e como o dataset foi construído.

4. **Treinamento do Modelo**
   https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki/Treinamento-do-Modelo
   Passo a passo para importar o CSV, treinar o modelo no Vertex AI e ativar o endpoint.

5. **App Android com Vertex AI ML Kit**
   https://github.com/jeferson-scheibler/moodmap-vertex-ai/wiki/App-Android-com-Vertex-AI-ML-Kit
   Guia prático de como criar o app, configurar câmera, capturar dados, analisar emoções e integrar com o Vertex AI.

---

## 🚀 Requisitos Básicos

- Conta Google Cloud com faturamento ativado
- Projeto criado no GCP
- Permissões para criar endpoints no Vertex AI
- Android Studio instalado
- Dispositivo com câmera frontal ou emulador com suporte

---

## 📂 Repositório

- `app/` → código Android
- `scripts/` → geração de dados sintéticos
- `README.md` → explicações iniciais
- `wiki/` → conteúdo principal da documentação (via Wiki)

---

## 🤝 Contribuições

Sinta-se à vontade para abrir issues ou enviar PRs para melhorias!

---

## 📬 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais detalhes.
