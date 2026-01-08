# 📘 Générateur de Brochures d’Entreprise

## 📌 Aperçu

Ce projet est une **solution professionnelle complète** qui génère automatiquement une brochure d’entreprise de qualité.
À partir d’un **nom d’entreprise** et de son **site web principal**, le système :

- Extrait et analyse le contenu pertinent du site
- Identifie les pages les plus significatives (À propos, Produits, Carrière, etc.)
- Génère un contenu clair, structuré et de haute qualité

La brochure résultante peut être utilisée pour :
- **Les clients potentiels**
- **Les investisseurs**
- **Les futurs collaborateurs**

Ce projet illustre comment les **grands modèles de langage (LLMs)** peuvent résoudre des problèmes concrets en entreprise.

---

## 🎯 Enjeu Métier

Concevoir un produit capable de **créer automatiquement une brochure complète** à partir de :
- Un nom d’entreprise
- Le site web principal de l’entreprise

Le défi ne se limite pas à la génération de contenu, mais consiste surtout à **déterminer quelles informations sont réellement pertinentes** sur un site réel et à les transformer en un document professionnel cohérent.

---

## 🛠 Installation

1. Clonez ce dépôt sur votre machine locale :
   ```bash
   git clone https://github.com/votre-utilisateur/company-brochure-generator.git
   cd company-brochure-generator
   ```

2. Installez **uv** d’Astral, un gestionnaire de dépendances et d’environnement Python moderne et performant :
   ```bash
   pip install uv
   ```

3. Installez les dépendances du projet et synchronisez l’environnement avec :
   ```bash
   uv sync
   ```

4. Pour lancer le projet, utilisez la commande :
   ```bash
   uv run
   ```

---

## 🧠 Approche

### Étape 1 – Identification des Liens Pertinents

La première étape consiste à analyser la page d’accueil de l’entreprise pour déterminer quels liens sont pertinents pour la création de la brochure.

Un appel à **GPT-5-nano** est utilisé pour :
- Lire et interpréter tous les liens d’une page web
- Décider quels liens contiennent des informations métiers significatives
- Retourner le résultat sous forme de **JSON structuré**
- Convertir les URLs relatives (ex: `/a-propos`) en URLs absolues (ex: `https://entreprise.com/a-propos`)

Cette étape utilise le **one-shot prompting**, où le modèle reçoit un exemple explicite du JSON attendu.

Cette tâche est particulièrement adaptée à un LLM, car elle nécessite une **compréhension contextuelle et sémantique** qui serait extrêmement complexe à implémenter avec une logique de scraping classique basée sur des règles.

---

### Étape 2 – Extraction de Contenu & Génération de la Brochure

Une fois les pages pertinentes identifiées :
- Le contenu est extrait
- Les informations clés sont résumées et restructurées
- Une brochure polie est générée en langage naturel

Ce processus peut être adapté à de nombreux cas d’usage métiers, tels que :
- La génération de contenu marketing
- La documentation produit
- La préparation de supports pour investisseurs
- Les campagnes email personnalisées

---

### Étape 3 – Diffusion en Continu (Amélioration de la Qualité)

En tant qu’amélioration finale, le système supporte la **diffusion en continu des réponses d’OpenAI** (Stream), permettant :
- Une génération progressive du contenu
- Un effet d’animation « machine à écrire » familier
- Une meilleure expérience utilisateur pour les brochures longues

---

## 💡 Pourquoi les LLMs ?

Ce projet met en lumière une force clé des LLMs :
> Les tâches nécessitant **jugement, détection de pertinence et compréhension nuancée** sont bien plus faciles et robustes lorsqu’elles sont déléguées à un modèle de langage.

Tenter de répliquer cette logique avec des méthodes classiques de parsing et des heuristiques serait fragile, complexe et sujet à erreurs.


---

## 🚀 Applications Réelles

Cette structure de projet peut être réutilisée dans de nombreux domaines :
- Génération automatique de brochures marketing
- Pipelines de transformation site-web → pitch deck
- Outils d’intelligence d’entreprise
- Plateformes d’automatisation de contenu pilotées par l’IA

---

## 📬 Support

Si vous avez des questions, des idées ou des problèmes en explorant ce projet, n’hésitez pas à nous contacter.
Ce dépôt est conçu à la fois comme un **projet pédagogique** et un **prototype métier réaliste**.
