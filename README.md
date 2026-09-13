# 6KO Production — Business Plan interactif

> Un business plan web immersif, autonome et interactif pour présenter le projet **6KO Production** à des partenaires, sponsors, financeurs et professionnels de la musique.

![Statut](https://img.shields.io/badge/statut-prototype%20op%C3%A9rationnel-1f9d8a)
![Version](https://img.shields.io/badge/version-V11-6f42c1)
![HTML](https://img.shields.io/badge/HTML-autonome-e34f26)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-f7df1e)
![Dépendances](https://img.shields.io/badge/d%C3%A9pendances-aucune-2ea44f)

---

## À propos du projet

**6KO Production** est présenté ici sous la forme d'un business plan web plutôt que d'un document statique classique.

L'objectif est double :

- exposer clairement la **vision artistique et économique** du projet ;
- fournir un véritable **outil d'aide à la décision**, avec hypothèses, financement, trésorerie, risques, partenaires et preuves à réunir avant lancement.

Le projet pilote **ONMANEK** sert de cas concret pour tester le modèle avant une montée en puissance plus large de 6KO Production.

Le document adopte volontairement une règle de prudence :

> **Une audience déclarée n'est pas une preuve. Une aide espérée n'est pas un financement. Un sponsor intéressé n'est pas un contrat.**

---

## Fonctionnalités principales

### Présentation immersive

- direction artistique inspirée de l'univers musical et du label indépendant ;
- mode **Scène** et mode **Clair** ;
- animations, halos, spectres et effets visuels autour de l'artiste ;
- bouton **FX LIVE** pour activer ou désactiver l'expérience animée ;
- navigation fluide entre les différentes parties du business plan ;
- responsive design pour ordinateur, tablette et smartphone.

### Business plan structuré

Le document est organisé autour de plusieurs blocs décisionnels :

1. **Audit** — niveau de préparation du projet et preuves manquantes ;
2. **Projet pilote ONMANEK** — concept, contenus avant / pendant / après et audience ;
3. **Marché** — contexte de l'industrie musicale et données de référence ;
4. **Modèle économique** — partenariats, précommandes, concerts, merchandising, droits et aides ;
5. **Financement** — budget, ressources réellement acquises et seuil de lancement ;
6. **Partenaires** — offres sponsor, contreparties et mesure de performance ;
7. **Aides** — dispositifs potentiellement mobilisables selon l'éligibilité réelle ;
8. **Exécution** — feuille de route sur 120 jours, risques, gouvernance et pièces à réunir.

### Outils interactifs

- scénarios budgétaires modifiables ;
- calcul automatique du **budget total** ;
- suivi du **financement réellement prouvé** ;
- calcul de l'écart restant à financer ;
- règle de décision automatique selon le taux de couverture ;
- test de trésorerie sur plusieurs mois ;
- stress-test du modèle économique ;
- checklist des preuves à réunir avant lancement ;
- sauvegarde locale des données saisies grâce à `localStorage` ;
- impression / export PDF depuis le navigateur.

---

## Philosophie financière

Le projet ne considère comme disponibles que les ressources :

- déjà encaissées ;
- contractualisées ;
- ou officiellement notifiées.

Les promesses orales, aides simplement demandées et revenus de streaming estimés ne sont pas considérés comme du financement acquis.

La logique de décision repose notamment sur les seuils suivants :

| Couverture du budget | Décision |
|---|---|
| **< 80 %** | Ne pas engager les dépenses |
| **80 à 99 %** | Préproduction réversible uniquement |
| **100 %** | Lancement possible sous réserve des autres preuves |

Cette approche cherche à limiter le risque de démarrer une production sur des recettes hypothétiques.

---

## Projet pilote : ONMANEK

**ONMANEK** constitue le premier cas d'usage du modèle 6KO Production.

Le dispositif éditorial repose sur une pièce centrale — le clip — accompagnée d'un écosystème de contenus :

- **avant** : teasers, stories, intention artistique ;
- **pendant** : coulisses, Reels, journal de production ;
- **après** : making-of, vlog et contenus de relance.

L'objectif est de transformer une sortie musicale ponctuelle en une campagne cohérente et mesurable.

---

## Architecture technique

Le projet est volontairement léger et portable.

```text
6KO_Business_Plan_Signature_V11_LightScene.html
README.md
```

Le fichier principal contient directement :

- le HTML ;
- les styles CSS ;
- le JavaScript ;
- les animations ;
- les images intégrées au format `data:` ;
- les composants interactifs.

Aucun framework, bundler ou package manager n'est nécessaire.

### Technologies

- **HTML5**
- **CSS moderne**
- **JavaScript vanilla**
- **Canvas API** pour certains effets visuels
- **Intersection Observer** pour les animations d'apparition
- **LocalStorage API** pour la persistance locale
- CSS `prefers-reduced-motion` pour la prise en compte de l'accessibilité liée aux mouvements

---

## Lancer le projet localement

### Méthode la plus simple

Télécharger le fichier :

```text
6KO_Business_Plan_Signature_V11_LightScene.html
```

puis l'ouvrir directement dans un navigateur moderne.

### Avec un petit serveur local

Pour éviter les différences de comportement entre navigateurs, il est possible de lancer un serveur HTTP local.

Avec Python :

```bash
python -m http.server 8000
```

Puis ouvrir :

```text
http://localhost:8000/6KO_Business_Plan_Signature_V11_LightScene.html
```

---

## Publication avec GitHub Pages

Le projet étant entièrement statique, il peut être publié très facilement avec **GitHub Pages**.

### 1. Renommer le fichier principal

Pour une URL plus propre, renommer :

```text
6KO_Business_Plan_Signature_V11_LightScene.html
```

en :

```text
index.html
```

### 2. Activer GitHub Pages

Dans le dépôt GitHub :

```text
Settings
└── Pages
    └── Build and deployment
        └── Deploy from a branch
```

Choisir ensuite la branche principale (`main`) et le dossier racine (`/`).

Le site sera alors accessible à l'adresse fournie par GitHub Pages.

---

## Données et confidentialité

Le projet ne nécessite pas de serveur ni de base de données distante.

Les informations saisies dans les simulateurs sont conservées localement dans le navigateur via `localStorage`.

Elles ne sont donc pas automatiquement envoyées vers un service externe par l'application elle-même.

> Attention : les liens vers des sources externes ouvrent naturellement les sites concernés dans le navigateur.

---

## Sources et traçabilité

Le business plan distingue les données de marché publiques des données propres au projet.

Les références intégrées dans l'interface incluent notamment :

- **SNEP** — marché français de la musique enregistrée ;
- **CNM** — usages de la musique et dispositifs d'aide ;
- **Adami** ;
- **Spedidam** ;
- **Spotify Loud & Clear** ;
- **Service-Public.fr** pour les éléments juridiques liés aux structures ;
- **W3C** pour les principes d'accessibilité et de contraste.

Les conditions des aides évoluent : toute demande doit être vérifiée à nouveau sur les sources officielles avant dépôt.

---

## Accessibilité et lisibilité

Une attention particulière est portée à :

- la lisibilité des textes ;
- la distinction entre mode sombre et mode clair ;
- le contraste des cartes, tableaux et indicateurs ;
- la navigation clavier ;
- la réduction des animations lorsque cela est nécessaire ;
- l'adaptation aux écrans mobiles.

Le bouton **FX LIVE** permet également de contrôler l'intensité de l'expérience visuelle.

---

## État du projet

Le projet est **fonctionnel** mais reste un dossier de décision évolutif.

Certaines données doivent être remplacées ou complétées par des preuves réelles avant toute présentation définitive à un financeur :

- exports Analytics datés ;
- devis réels ;
- contrats ou lettres d'intention partenaires ;
- validation du montage juridique et fiscal ;
- chaîne de droits et propriété des masters ;
- stratégie de distribution ;
- calendrier de production ;
- trésorerie réelle ;
- assurances et responsabilités ;
- KPI issus des premières campagnes.

Le document doit donc être compris comme un **outil de pilotage et de préparation**, et non comme une garantie de réussite économique.

---

## Améliorations envisagées

- [ ] intégrer les Analytics certifiés de 6KO ;
- [ ] remplacer les hypothèses budgétaires par des devis réels ;
- [ ] documenter les premiers résultats de prospection sponsor ;
- [ ] intégrer les contrats / lettres d'intention signés ;
- [ ] compléter les données de conversion après lancement d'ONMANEK ;
- [ ] ajouter un historique des versions du business plan ;
- [ ] mettre en place une validation terrain avec partenaires et professionnels de la musique ;
- [ ] éventuellement séparer à terme les données métier de la couche de présentation.

---

## Contribution

Le dépôt est actuellement centré sur le développement du projet 6KO Production.

Pour toute contribution :

1. créer une branche dédiée ;
2. effectuer les modifications ;
3. vérifier le rendu en mode clair et en mode scène ;
4. tester les simulateurs ;
5. vérifier le responsive ;
6. ouvrir une Pull Request en décrivant précisément les changements apportés.

Les modifications de contenu financier, juridique ou de marché doivent être accompagnées d'une source ou d'un justificatif vérifiable.

---

## Licence

Aucune licence open source n'est définie par défaut dans ce dépôt.

Sauf ajout ultérieur d'un fichier `LICENSE`, le code, les visuels, le contenu éditorial et l'identité graphique restent protégés par le droit d'auteur applicable.

---

## Avertissement

Ce projet constitue un outil de présentation et d'aide à la décision.

Il ne remplace pas :

- un expert-comptable ;
- un avocat ou juriste ;
- un conseil fiscal ;
- un conseil spécialisé dans le financement de la musique.

Les chiffres, hypothèses, dispositifs d'aide et règles juridiques doivent être vérifiés avant toute décision engageante.

---

<p align="center">
  <strong>6KO Production</strong><br>
  Musique · Image · Stratégie · Preuve
</p>
