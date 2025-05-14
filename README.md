# 🧠 Chat com Documentos via IA (RAG com Langchain + Hugging Face)

Este projeto implementa um pipeline de RAG (Retrieval-Augmented Generation) que permite **fazer perguntas em linguagem natural sobre documentos PDF**, utilizando **modelos de linguagem (LLMs)**, **vetorização semântica** e a biblioteca **Langchain**. O modelo de linguagem roda localmente, sem necessidade de API da OpenAI.

---

## 📌 Objetivo

Permitir que o usuário envie documentos PDF e, com base no conteúdo carregado, possa fazer perguntas com resposta gerada por uma IA treinada para compreender linguagem natural. Tudo isso utilizando modelos gratuitos da Hugging Face, de forma **offline** e transparente.

---

## 🚀 Tecnologias Utilizadas

| Componente            | Ferramenta / Biblioteca                    |
|------------------------|--------------------------------------------|
| LLM                   | `google/flan-t5-base` (local, via Transformers) |
| Embeddings            | `InstructorEmbedding` (`hkunlp/instructor-xl`) |
| Vetor Semântico       | `FAISS`                                    |
| Pipeline de IA        | `Langchain`                                |
| PDF Loader            | `PyPDFLoader` (Langchain)                  |
| Interface             | `Jupyter Notebook` via Anaconda            |
| Ambiente              | `Python 3.10+`, `.env`                     |

---

## 📂 Estrutura de Pastas

chat-com-documentos-rag/
├── chat_com_documentos.ipynb # Notebook principal
├── data/documentos
│ └── contrato_ficticio.pdf # Documento PDF de exemplo
├── faiss_index/ # Base vetorizada salva (gerada no processo)
├── .env # Token Hugging Face (não incluído no Git)
├── .gitignore # Arquivos ignorados
├── requirements.txt # Bibliotecas necessárias
└── README.md # Este arquivo
