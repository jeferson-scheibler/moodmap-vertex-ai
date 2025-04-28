# ☁️ MoodMap – Integração Android + Vertex AI

Este repositório demonstra o uso do **Google Vertex AI** integrado a um aplicativo Android real.  
A proposta é capturar expressões faciais do usuário, analisar o som ambiente, identificar o **estado emocional** e sugerir **lugares** próximos adequados ao humor detectado.

## 📚 Introdução

**Vertex AI** é a **plataforma completa** de inteligência artificial da **Google Cloud**.

Com o Vertex AI, **não precisamos** nos preocupar com servidores, infraestrutura, balanceamento de carga ou complexidades técnicas pesadas de Machine Learning — ele gerencia tudo isso para nós.

O **objetivo** do Vertex AI é simples:  
➡️ Tornar mais fácil **treinar**, **implementar** (deploy) e **usar** **modelos de Machine Learning** em **produção**, com **poucas linhas de código** e **alta performance**.

---

## 🧩 Principais funcionalidades do Vertex AI

| Funcionalidade | Explicação Simples |
|:--------------|:------------------|
| **AutoML** | Treine modelos de alta qualidade automaticamente com base em seus dados, sem precisar escrever código de IA |
| **Custom Training** | Faça treinamentos personalizados, usando seus próprios algoritmos e ambientes customizados |
| **Vertex AI Workbench** | Tenha um ambiente integrado (tipo um Jupyter Notebook avançado) para prototipar seus modelos |
| **Dataset Management** | Armazene e gerencie datasets para Machine Learning |
| **Model Deployment** | Faça o deploy dos seus modelos em Endpoints escaláveis para consumir em apps reais |
| **MLOps Integrado** | Versionamento de modelos, monitoramento, controle de performance e atualizações contínuas (ciência de dados de verdade!) |

---

## 🔥 As possibilidades do Vertex AI

O Vertex AI não serve apenas para “treinar modelos”.

Ele possibilita **construir soluções de ponta a ponta**, como:

- 📸 **Classificação de imagens** (reconhecimento de objetos, faces, produtos)
- 🧾 **Análise de texto** (sentimento, tradução, resumo automático)
- 🏥 **Predição de eventos** (prognóstico de doenças, falhas de máquinas)
- 🛒 **Recomendação de produtos** (como Amazon, Netflix)
- 🗺️ **Análise de localização** (sugerir melhores locais com base em comportamento, como estamos fazendo!)
- 🎤 **Processamento de áudio** (reconhecimento de fala, análise de sons ambientais)
- 🎬 **Detecção em vídeos** (identificar movimentos, objetos, pessoas)

---
## 📈 Por que usar o Vertex AI e não treinar modelos locais?

| Vertex AI | Treinar Localmente |
|:---------|:------------------|
| Escala ilimitada na nuvem 🌎 | Limitação de hardware local |
| Modelo gerenciado, com alta disponibilidade | Modelo sujeito a falhas de servidor |
| AutoML encontra o melhor modelo para seus dados | Treinamento manual, exige expertise em ML |
| Fácil integração com apps via API | Necessidade de configurar servidores de inferência |

---

## No nosso projeto: Como usamos o Vertex AI?

**No MoodMap**, usamos o Vertex AI para:

| Etapa | Detalhes |
|:-----|:---------|
| 🎯 **Objetivo** | Criar um modelo de Machine Learning que detecta a emoção do usuário com base nos dados faciais capturados (sorriso, olhos, ângulos, landmarks) |
| 📂 **Entrada de dados** | Um CSV com milhares de exemplos de combinações de expressões faciais e o humor associado |
| 🏋️ **Treinamento** | Usamos **AutoML Tabular**: o Vertex AI treinou automaticamente o melhor modelo |
| ☁️ **Deploy** | Fizemos o deploy do modelo em um **Endpoint** gerenciado pela Google Cloud |
| 🔥 **Inferência no app** | Nosso app Android envia dados faciais para o Vertex AI e recebe de volta a emoção predita |

---

## 🛠️ Arquivo base (.csv)

O dataset utilizado para treinar o modelo está incluído no projeto no diretório: /datasets/treinamento_humor_unimap.csv

Esse arquivo contém **exemplos sintéticos** com 11 atributos faciais para classificação de humor.  
Você pode usá-lo para **recriar o experimento** facilmente no Vertex AI.

---

## 🚀 Passo a passo detalhado para recriar o modelo no Vertex AI

### 1. Subir o dataset no Vertex AI

- Acesse o console do [Vertex AI](https://console.cloud.google.com/vertex-ai)
- Vá em **Datasets** → **Create Dataset**
- Escolha **Tabular Dataset**
- Faça o upload do arquivo `treinamento_humor_unimap.csv`
- Defina a coluna alvo (**Target Column**) como `humor`
- Avance e crie o Dataset

---

### 2. Treinar o modelo AutoML

- Dentro do seu Dataset, clique em **Train New Model**
- Escolha **AutoML** como tipo de treinamento
- Nomeie o modelo (ex: `modelo_moodmap`)
- Deixe as configurações padrão ou ajuste conforme desejar
- Inicie o treinamento

> 🕒 O treinamento pode levar de alguns minutos a algumas horas dependendo da configuração.

---
### 3. Fazer o deploy do modelo

- Após o treinamento, clique em **Deploy to Endpoint**
- Crie um **Endpoint** (ou use um existente)
- Aguarde a implantação ser concluída
- Anote o **ID do Endpoint** e o **região** (ex: `southamerica-east1`)

---
### 4. Atualizar o aplicativo Android

No seu projeto Android:

- Atualize o código para apontar para o novo `endpointId` e `projectId`
- Certifique-se que a requisição de inferência esteja no formato com todos os valores sendo enviados como string no JSON.
