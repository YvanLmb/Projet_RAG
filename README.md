# Projet RAG : Recherche et Génération (RAG) avancée sur le dataset FQuAD

## 📚 Description
Ce projet est une implémentation d'un modèle de **Recherche et Génération (RAG)** qui teste et compare différentes méthodes avancées d'approches RAG sur le dataset français **FQuAD**. L'objectif principal est d'évaluer des techniques variées de traitement, d'interrogation et de génération sur des questions-réponses basées sur des documents en français.

---

## 🚀 Objectifs du Projet
1. **Évaluer les approches avancées de RAG** :
   - Comparer différentes méthodes, incluant le BM25, la recherche dense avec embeddings générés par **Sentence Transformers**, et des recherches hybrides.
   - Intégrer des techniques avancées de découpage de texte (chunking).
2. **Explorer des configurations de modèles** :
   - Tester l'impact des configurations de température sur la génération de réponses.
   - Utiliser des modèles instructifs comme **Mistral-7B** pour la génération.
3. **Utilisation du dataset FQuAD** :
   - Le dataset FQuAD est une version française de SQuAD (Stanford Question Answering Dataset).
   - Il contient des paires question-réponse basées sur des contextes extraits de Wikipédia.
   - Objectif : Répondre à des questions en exploitant des passages contextuels du dataset.

---

## 🛠️ Méthodologie
### 1. Prétraitement des données
- Extraction et découpage des contextes en chunks pour une gestion optimale.
- Indexation des données pour la recherche (BM25, dense avec embeddings, hybride).

### 2. Méthodes explorées
- **No Processing** : Pas de découpage préalable, interrogation directe.
- **Early Chunking** : Découpage avant l'interrogation, avec analyse de chaque chunk.
- **Hybrid Search** : Combinaison pondérée des recherches BM25 et dense (embeddings Sentence Transformers).
- **Late Chunking** : Découpage après une recherche initiale.

### 3. Génération d'Embeddings
- Les embeddings des textes ont été générés à l'aide de **Sentence Transformers** ([HuggingFace SentenceTransformers](https://www.sbert.net/)).
- Modèle utilisé : `sentence-transformers/all-MiniLM-L6-v2`, adapté pour des tâches de recherche dense et de similarité.

### 4. Évaluation des résultats
- Comparaison des méthodes avec les métriques suivantes :
  - **Exact Match (EM)** et **F1 Score**
  - **BERTScore**
  - **ROUGE-1, ROUGE-2, ROUGE-L**
  - **BLEU**



## 🔧 Technologies Utilisées
- **Langages** : Python
- **Frameworks et librairies** :
  - LangChain pour le traitement des documents.
  - PyTorch et Transformers pour la gestion des modèles.
  - **Sentence Transformers** pour la génération d'embeddings.
  - BM25Okapi et FAISS pour la recherche.
  - Evaluation avec **BERTScore**, **ROUGE**, et **BLEU**.
- **Dataset** : FQuAD
- **Modèle** :
  - Génération de réponses : [Mistral-7B-Instruct-v0.1](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1)
  - Embeddings : [sentence-transformers/all-MiniLM-L6-v2](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)

---


---

## 🤝 Contributeurs
- **YvanLmb** : Créateur principal

---
