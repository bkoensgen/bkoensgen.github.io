<p align="center">
  <img src="assets/photo-profil-robots.jpg" alt="Photo du projet Robo-Pointer" width="350"/>
</p>

# Benjamin Koensgen

## Ingénieur en Intelligence Artificielle & Robotique

*De la conception de pipelines IA à leur incarnation physique en robotique.*

---

J'ai quitté mon poste avec une conviction : je devais maîtriser par moi-même les technologies d'IA qui commençaient à tout redéfinir. Mon approche a été simple : d'abord le "cerveau" logiciel, puis le "corps" physique.

---

## Projets & Réalisations

Ici, un aperçu des projets concrets qui ont marqué ce parcours de R&D.

### Projet Robo-Pointer : Cycle Complet de la Mécatronique 🦾

<a href="[LIEN VIDÉO YOUTUBE/VIMEO]" target="_blank">
  <img src="[LIEN IMAGE THUMBNAIL DE LA VIDÉO]" alt="Démonstration du Robo-Pointer" style="max-width:100%;">
</a>

> J'ai conçu, imprimé en 3D et assemblé ce bras 6-axes, puis développé le pipeline ROS 2 de A à Z pour le contrôle et le suivi d'objet par vision. C'est la démonstration de ma capacité à gérer l'intégralité du cycle mécatronique.

**Technologies :** `ROS 2` `C++` `Python` `OpenCV` `Conception CAO (SolidWorks/Inventor)` `Impression 3D`

**[Voir le code et la documentation sur GitHub] →** `https://github.com/bkoensgen/robo-pointer-so100`

### Projet AudioBuy : Pipeline de Données et Analyse par LLM 🧠

```mermaid
graph TD
    %% Configuration des styles épurés
    classDef input fill:#4A90E2,stroke:#357ABD,stroke-width:2px,color:#fff,font-weight:bold
    classDef processing fill:#5B9BD5,stroke:#4A90E2,stroke-width:2px,color:#fff,font-weight:bold
    classDef ai fill:#7B68EE,stroke:#6A5ACD,stroke-width:3px,color:#fff,font-weight:bold
    classDef data fill:#9B9B9B,stroke:#777777,stroke-width:2px,color:#fff,font-weight:bold
    classDef success fill:#5CB85C,stroke:#449D44,stroke-width:2px,color:#fff,font-weight:bold
    classDef failure fill:#D9534F,stroke:#C9302C,stroke-width:2px,color:#fff,font-weight:bold

    %% === COLLECTE DE DONNÉES ===
    subgraph Input [" COLLECTE MULTI-SOURCE "]
        direction TB
        Web["Sources Web<br/>Annonces & Prix"]
        Images["Images Produits<br/>Visuels & Texte"]
        
        WebScraper["Web Scraping<br/>Python + Selenium"]
        OCREngine["Analyse d'Image (OCR)<br/>Google Vision API"]
        
        RawData["DONNÉES BRUTES<br/>Format Unifié"]
    end

    %% === TRAITEMENT IA ===
    subgraph AI [" INTELLIGENCE ARTIFICIELLE "]
        direction TB
        PromptDesign["Prompt Engineering<br/>Requête Structurée"]
        CoreLLM["LLM ENGINE<br/>OpenAI / Claude"]
        StructuredOutput["OUTPUT JSON<br/>Marque • Modèle • État"]
    end

    %% === LOGIQUE MÉTIER ===
    subgraph Logic [" ANALYSE & DÉCISION "]
        direction TB
        MarketDB[("BASE MARCHÉ<br/>Prix Référence")]
        Analyzer{"COMPARATEUR<br/>Logique Métier"}
    end

    %% === ACTIONS ===
    subgraph Output [" ACTIONS FINALES "]
        direction TB
        Alert["OPPORTUNITÉ<br/>Alerte Telegram"]
        Reject["REJET<br/>Pas Intéressant"]
    end

    %% === FLUX PRINCIPAL ===
    Web --> WebScraper
    Images --> OCREngine
    WebScraper --> RawData
    OCREngine --> RawData
    
    RawData --> PromptDesign
    PromptDesign --> CoreLLM
    CoreLLM --> StructuredOutput
    
    StructuredOutput --> Analyzer
    MarketDB --> Analyzer
    
    Analyzer -->|"DEAL TROUVÉ"| Alert
    Analyzer -->|"TROP CHER"| Reject

    %% === APPLICATION DES STYLES ===
    class Web,Images,WebScraper,OCREngine input
    class PromptDesign,CoreLLM,StructuredOutput ai
    class RawData data
    class Analyzer,MarketDB processing
    class Alert success
    class Reject failure
```

> Un système autonome développé pour identifier des opportunités de marché en temps réel. Le pipeline scrape les données (texte et images), les analyse via un LLM pour en extraire la structure, et les compare à une base de données de prix pour une décision automatisée.

**Technologies :** `Python` `LLMs (OpenAI API)` `Web Scraping` `Google Vision (OCR)` `Bases de Données (SQL)`

**[Voir la présentation technique sur GitHub] →** `[https://github.com/bkoensgen/Audiobuy-showcase.git]`

### Contribution Nav2 : Optimisation pour la Robotique Professionnelle 🏆

![Snippet de code Nav2]([LIEN IMAGE SNIPPET AVANT/APRÈS])

> Pour résoudre un problème d'inefficacité énergétique dans un standard mondial de la robotique, j'ai implémenté une nouvelle API au cœur de Nav2. Cette solution permet d'activer les nœuds de détection à la demande, optimisant ainsi les ressources des robots embarqués.

**Technologies :** `C++` `ROS 2` `Architecture Logicielle` `Tests Unitaires (GTest)`

**[Voir la Pull Request sur GitHub (#5218)] →** `https://github.com/ros-navigation/navigation2/pull/5218`

---

## Contact & Liens

N'hésitez pas à me contacter.

[LinkedIn](https://www.linkedin.com/in/benjamin-koensgen) | [GitHub](https://github.com/bkoensgen) | [E-mail](mailto:bkoensgen@gmail.com)