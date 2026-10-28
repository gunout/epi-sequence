<div align="center">

# EPI-SEQUENCE PRO

> Plateforme d'aide a la decision clinique pour la gestion des crises epileptiques
> Hologramme neuronal 3D - Prediction IA - Sequenceur CTAG - Protocole Etat de Mal

![Version](https://img.shields.io/badge/version-8.0.0-00e5ff)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-active-00ff9d)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-r128-black)
![Chart.js](https://img.shields.io/badge/Chart.js-4.4.0-FF6384)
</div>

---

## Sommaire

- [Presentation](#presentation)
- [Fonctionnalites cles](#fonctionnalites-cles)
- [Architecture 3D neuronale](#architecture-3d-neuronale)
- [Sequenceur CTAG](#sequenceur-ctag)
- [Prediction IA](#prediction-ia)
- [Protocole Etat de Mal](#protocole-etat-de-mal)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Stack technique](#stack-technique)
- [Structure du projet](#structure-du-projet)
- [Roadmap](#roadmap)
- [Contribution](#contribution)
- [Avertissement medical](#avertissement-medical)
- [Licence](#licence)

---

## Presentation

**EPI-SEQUENCE PRO** est une demonstration d'interface clinique avancee dediee a la **prise en charge des crises epileptiques** et de **l'etat de mal epileptique (Status Epilepticus)**. Concue comme un outil d'aide a la decision pour neurologues, urgentistes et internes, elle combine :

- Un **hologramme neuronal 3D realiste** visualisant la propagation de la decharge epileptique
- Un **moteur de prediction IA** estimant le risque de crise imminente (0-24h)
- Un **sequenceur CTAG** (Clinical Timeline & Algorithm Guide) qui adapte le protocole SE en temps reel
- Un **tableau de bord multimodal** (EEG, wearables, scores cliniques, feedback IA)

> **Attention** : Ce projet est une demonstration technologique. Il ne constitue en aucun cas un dispositif medical certifie et ne doit pas etre utilise pour un usage clinique reel sans validation reglementaire appropriee.

---

## Fonctionnalites cles

### Hologramme neuronal futuriste
- **280 neurones** avec somas, dendrites et connexions synaptiques courbes
- **120 potentiels d'action** animes le long des axones
- **Recrutement neuronal dynamique** : propagation de la decharge critique en temps reel (0-100%)
- **Eclairs electriques proceduraux** entre neurones lors des decharges
- **Foyer critique** avec halos, ondes de choc et pulsations
- **800 particules ambiantes** + grille holographique
- Controle de la camera (3D / Axial / Coronal / Sagittal)

### Sequenceur CTAG (Clinical Timeline & Algorithm Guide)

9 etapes dynamiques qui s'adaptent a la duree ecoulee et aux doses administrees :

| Temps | Etape | Statut |
|-------|-------|--------|
| 0-1 min | Reconnaissance & Securisation | Auto |
| 1-5 min | Position Laterale de Securite | Auto |
| **5 min** | **Appel SAMU / 15** | Alerte |
| 5-10 min | Benzodiazepine 1ere dose | Manuel |
| 10-15 min | 2eme dose si echec | Manuel |
| 15-20 min | Examens urgents | Manuel |
| **20-30 min** | **2eme ligne antiepileptique** | Alerte |
| **> 30 min** | **Etat de mal refractaire** | Alerte |
| Post-critique | Surveillance & Reevaluation | Manuel |

### Prediction IA
- Jauge de risque 0-24h avec code couleur (vert/jaune/orange/rouge)
- **Facteurs contributifs ponderes** : sommeil, observance, stress, EEG pre-ictal, alcool
- Historique des predictions avec validation (crise confirmee / pas de crise)
- Recalcul temps reel

### Tableau de bord clinique
- **Charts** : frequence des crises, amplitude EEG, taux plasmatiques des antiepileptiques, distribution des types
- **Scores** : Glasgow, STESS (pronostique), EEG ictal, etiologie en cours
- **Therapie** : recommandations 1ere/2eme/3eme ligne, contre-indications, cas grossesse
- **Calendrier RCP** interactif avec evenements
- **Modules educatifs** personnalises avec correlations statistiques (r = 0.72 sommeil, r = -0.35 activite physique)

### Integration wearables
- EEG portable, montre connectee, smartphone, capteur de sommeil
- Statuts temps reel (online / warn / offline)
- Alertes de detection et limites documentees

### Teleconsultation RCP (WebRTC)
- Flux video local via `getUserMedia`
- 3 pairs distants simules
- Controles micro / camera / partage d'ecran / enregistrement
- Latence et statut peers affiches

---

## Architecture 3D neuronale

```
                    +-----------------------------+
                    |   Reseau neuronal (280)     |
                    |  +-----------------------+  |
                    |  |  Somas (spheres)      |  |
                    |  |  Dendrites (lignes)   |  |
                    |  |  Axones (Bezier)      |  |
                    |  +-----------------------+  |
                    |            |                |
                    |  +---------v---------+      |
                    |  | Potentiels action |      |
                    |  |  (120 particules) |      |
                    |  +---------+---------+      |
                    |            |                |
                    |  +---------v---------+      |
                    |  |  Foyer critique   |      |
                    |  |  + ondes de choc  |      |
                    |  +-------------------+      |
                    +-----------------------------+
```

**Comportements dynamiques :**
- Les neurones proches du foyer (inferieur au seuil calcule) passent en mode **critique** (rouge, x1.4, pulsation intense)
- A chaque `fire`, un **arc electrique** est genere vers un neurone voisin
- Le slider **"Recrutement neuronal"** (0-100%) controle directement la propagation
- Le compteur topbar affiche `(neurones sains) / (total)`

---

## Prediction IA

Le moteur de prediction utilise un **modele de scoring pondere** (simule) :

| Facteur | Poids |
|---------|-------|
| Sommeil inferieur a 6h (3 derniers jours) | **+22%** |
| Observance therapeutique inferieure a 80% | **+18%** |
| Stress rapporte (8/10) | **+12%** |
| Activite EEG pre-ictale detectee | **+9%** |
| Alcool (2 verres hier) | **+7%** |
| Respect des horaires de prise | **-8%** |
| Activite physique reguliere | **-5%** |

**Sensibilite revendiquee** : 87.8% (fenetre 0-24h, fausses alarmes ~0.8/jour - valeurs simulees).

---

## Protocole Etat de Mal

Le protocole suit les recommandations internationales :

### 1ere ligne (5-30 min)
- **Lorazepam** IV 0.1 mg/kg (max 4 mg)
- OU **Midazolam** buccal 0.5 mg/kg
- OU **Diazepam** rectal 0.5 mg/kg

### 2eme ligne (superieur a 20 min)
- **Levetiracetam** 60 mg/kg IV (max 4500 mg)
- OU **Phenytoine** 20 mg/kg IV
- OU **Valproate** 40 mg/kg IV

### 3eme ligne (superieur a 30-60 min)
- **Propofol** ou **Thiopental** en reanimation
- EEG continu obligatoire

### Contre-indications absolues
- Ne **rien** introduire dans la bouche
- Ne pas **immobiliser** le patient
- Ne pas **retarder** les benzodiazepines

### Grossesse
- **Eviter le valproate** (teratogene)
- Preferer **Levetiracetam** ou **Lamotrigine**

---

## Installation

Aucune dependance a installer. Clonez simplement le depot et ouvrez `index.html`.

```bash
git clone https://github.com/gunout/epi-sequence.git
cd epi-sequence
```

### Option 1 - Ouverture directe
```bash
# Ouvrir index.html dans votre navigateur
open index.html      # macOS
start index.html     # Windows
xdg-open index.html  # Linux
```

### Option 2 - Serveur local (recommande pour WebRTC)
```bash
# Python 3
python -m http.server 8080

# Node.js
npx serve .

# PHP
php -S localhost:8080
```

Puis ouvrir http://localhost:8080

> **Note** : WebRTC (`getUserMedia`, `getDisplayMedia`) necessite **HTTPS** ou **localhost**. En cas d'absence de camera, l'application bascule automatiquement en mode simulation.

---

## Utilisation

### Connexion
1. Choisissez un role : **Neurologue**, **Urgentiste**, **Interne** ou **Admin**
2. Entrez vos identifiants (valeurs par defaut disponibles)
3. Validez le code 2FA (6 chiffres, n'importe quelle valeur)

### Navigation

| Panneau | Contenu |
|---------|---------|
| **Gauche** | Liste des dossiers patients (EPI-023, 041, 058, 072) |
| **Centre-gauche** | Sequenceur CTAG + parametres temps reel |
| **Centre** | Hologramme neuronal 3D + overlays |
| **Droite** | 8 onglets (Prediction, Wearables, Education, Charts, Scores, Therapie, Calendrier, IA) |
| **Bas** | Selecteur de phase SE + timeline + actions |

### Interactions cles
- **Slider "Recrutement neuronal"** : anime la propagation de la crise dans le cerveau 3D
- **Slider "Duree ecoulee"** : declenche les alertes CTAG (5, 10, 20, 30 min)
- **Bouton Snapshot** : telecharge une capture PNG du canvas
- **Bouton RCP LIVE** : lance la teleconsultation WebRTC simulee
- **Bouton Recalculer** (onglet Prediction) : met a jour le risque
- **Bouton Re-entrainement** (onglet IA) : simule un cycle d'apprentissage

---

## Stack technique

| Composant | Technologie |
|-----------|-------------|
| **Rendu 3D** | Three.js r128 (CDN) |
| **Graphiques** | Chart.js 4.4.0 (CDN) |
| **WebRTC** | API native `getUserMedia` / `getDisplayMedia` |
| **Styling** | CSS pur (variables, animations, backdrop-filter) |
| **Logique** | JavaScript vanilla (ES6+) |
| **Polices** | SF Mono / Courier New (fallback) |

**Aucune etape de build.** Fichier HTML autonome.

---

## Structure du projet

```
epi-sequence/
+-- index.html      # Application complete (HTML + CSS + JS)
+-- LICENSE         # Licence MIT
+-- README.md       # Ce fichier
```

> Le projet est volontairement **monolithique** pour faciliter la demonstration et le deploiement en un seul fichier.

---

## Roadmap

### v8.0 (actuelle)
- [x] Hologramme neuronal 3D realiste
- [x] Sequenceur CTAG dynamique
- [x] Prediction IA avec facteurs ponderes
- [x] Integration wearables (simulee)
- [x] Modules educatifs personnalises
- [x] Teleconsultation RCP WebRTC

### v9.0 (a venir)
- [ ] Backend Node.js/Python pour donnees reelles
- [ ] Integration HL7 / FHIR
- [ ] Authentification OAuth2 + SSO hopital
- [ ] Persistance des sessions (IndexedDB)
- [ ] Mode multilingue (EN, DE, ES)
- [ ] Tests automatises (Jest + Playwright)

### v10.0 (exploratoire)
- [ ] Modele ML reel (TensorFlow.js) entraine sur donnees EEG open-source
- [ ] Import DICOM / EDF
- [ ] Export PDF des RCP
- [ ] Application mobile compagnon (React Native)

---

## Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. **Fork** le projet
2. Creez une branche (`git checkout -b feature/nouvelle-fonctionnalite`)
3. Commitez (`git commit -m 'feat: ajout de X'`)
4. Pushez (`git push origin feature/nouvelle-fonctionnalite`)
5. Ouvrez une **Pull Request**

### Convention de commits
Nous suivons [Conventional Commits](https://www.conventionalcommits.org/) :
- `feat:` nouvelle fonctionnalite
- `fix:` correction de bug
- `docs:` documentation
- `style:` formatage
- `refactor:` refactorisation
- `test:` tests

---

## Avertissement medical

> **EPI-SEQUENCE PRO est une demonstration technologique a visee educative et de recherche.**
>
> - **Ne constitue pas un dispositif medical** au sens du Reglement (UE) 2017/745 (MDR)
> - **Ne doit pas etre utilise** pour un diagnostic, un traitement ou une decision clinique reelle
> - **Les donnees affichees sont simulees** (patients fictifs, scores, predictions)
> - **Les protocoles affiches** s'inspirent des recommandations publiees mais ne remplacent pas le jugement clinique
>
> Pour tout usage clinique, une **certification MDR IIa** (ou superieure) et une **validation clinique** sont indispensables.

---

## Licence

Distribue sous licence **MIT**. Voir [LICENSE](https://github.com/gunout/epi-sequence/blob/main/LICENSE) pour plus d'informations.

```
MIT License

Copyright (c) 2026 gunout

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## Remerciements

- [Three.js](https://threejs.org/) - moteur 3D
- [Chart.js](https://www.chartjs.org/) - graphiques
- [Shields.io](https://shields.io/) - badges
- Communaute epileptologie francophone pour les references cliniques

---

<div align="center">

**Si ce projet vous interesse, n'hesitez pas a lui donner une etoile !**

[Signaler un bug](https://github.com/gunout/epi-sequence/issues) - [Proposer une fonctionnalite](https://github.com/gunout/epi-sequence/issues) - [Documentation](https://github.com/gunout/epi-sequence)

*Fait avec passion par [@gunout](https://github.com/gunout)*

</div>
