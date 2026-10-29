<!-- ============================================================ -->
<!--  GUNOUT — EPI-SEQUENCE PRO · NEON ROSE README                -->
<!-- ============================================================ -->

<p align="center">
  <a href="https://github.com/gunout/epi-sequence">
    <img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&weight=700&size=26&pause=800&color=FF2D95&background=0D001A00&center=true&vCenter=true&random=false&width=900&lines=%F0%9F%A7%A0+EPI-SEQUENCE+PRO;Neural+Hologram+%E2%80%A2+CTAG+%E2%80%A2+AI+Prediction;Futuristic+Clinical+Interface;Neon+Protocol+Online." alt="Typing SVG" />
  </a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/gunout/gunout/main/assets/images/divider_neon.svg" alt="Divider" />
</p>

<div align="center">

# 🧠 EPI-SEQUENCE PRO

**Interface médicale 3D interactive — Simulation de crises épileptiques en temps réel**

[![Version](https://img.shields.io/badge/version-9.4.0-FF2D95?style=for-the-badge)](https://github.com/gunout/epi-sequence)
[![Three.js](https://img.shields.io/badge/Three.js-0.160.0-FF69B4?style=for-the-badge&logo=three.js&logoColor=white)](https://threejs.org/)
[![License](https://img.shields.io/badge/license-MIT-FFB6D9?style=for-the-badge)](https://github.com/gunout/epi-sequence/blob/main/LICENSE)
[![Status](https://img.shields.io/badge/status-active-FF2D95?style=for-the-badge)](https://github.com/gunout/epi-sequence)

[![Stars](https://img.shields.io/github/stars/gunout/epi-sequence?style=for-the-badge&color=FF2D95&labelColor=0D001A)](https://github.com/gunout/epi-sequence/stargazers)
[![Forks](https://img.shields.io/github/forks/gunout/epi-sequence?style=for-the-badge&color=FF69B4&labelColor=0D001A)](https://github.com/gunout/epi-sequence/network)
[![Issues](https://img.shields.io/github/issues/gunout/epi-sequence?style=for-the-badge&color=FFB6D9&labelColor=0D001A)](https://github.com/gunout/epi-sequence/issues)
[![Last Commit](https://img.shields.io/github/last-commit/gunout/epi-sequence?style=for-the-badge&color=FF2D95&labelColor=0D001A)](https://github.com/gunout/epi-sequence/commits)
[![Code Size](https://img.shields.io/github/languages/code-size/gunout/epi-sequence?style=for-the-badge&color=FF69B4&labelColor=0D001A)](https://github.com/gunout/epi-sequence)

</div>

<p align="center">
  <img src="https://raw.githubusercontent.com/gunout/gunout/main/assets/images/divider_neon.svg" alt="Divider" />
</p>

---

## ⚡ `overview`

**EPI-SEQUENCE PRO** est une démonstration d'interface clinique avancée dédiée à la **prise en charge des crises épileptiques** et de **l'état de mal épileptique (Status Epilepticus)**.

Conçue comme un outil d'aide à la décision pour **neurologues**, **urgentistes** et **internes**, elle combine :

- 🧠 **Atlas cérébral 3D anatomique** — 437 structures, 563 meshes (source : Brain Project d'Itay Inbar)
- ⚡ **Arcs électriques néon** ancrés sur les structures corticales
- 📊 **Séquenceur CTAG** — protocole SE dynamique (0-60 min)
- 🎯 **Prédiction IA** — risque de crise à 24h
- 🩺 **HUD clinique complet** — scores Glasgow, STESS, EEG, RCP Live

> ⚠️ **Démonstration technologique** — Ne constitue pas un dispositif médical certifié.

---

## ✨ `features`

### 🧠 Hologramme neuronal futuriste

- **Cerveau anatomique complet** — 437 structures, 563 meshes Draco-compressés
- **Arcs électriques néon** (rouge/rose/jaune) ancrés sur les structures corticales
- **Recrutement neuronal dynamique** — propagation de la décharge en temps réel (0-100%)
- **Foyer critique** avec halos et pulsations
- **Contrôle caméra** — Rotation 360°, zoom limité, pan vertical
- **4 vues anatomiques** — 3D, Axial, Coronal, Sagittal
- **Mode Rayons X** — cortex transparent pour voir les structures internes
- **Couleurs anatomiques** — cortex rose, vaisseaux rouges, nerfs jaunes, ventricules bleus
- **Survol interactif** — identification des structures avec HUD

### 📊 Séquenceur CTAG (Clinical Timeline & Algorithm Guide)

| Temps | Étape | Statut |
|-------|-------|--------|
| 0-1 min | Reconnaissance & Sécurisation | Auto |
| 1-5 min | Position Latérale de Sécurité | Auto |
| **5 min** | **Appel SAMU / 15** | ⚠ Alerte |
| 5-10 min | Benzodiazépine 1ère dose | Manuel |
| 10-15 min | 2ème dose si échec | Manuel |
| 15-20 min | Examens urgents | Manuel |
| **20-30 min** | **2ème ligne antiépileptique** | ⚠ Alerte |
| **> 30 min** | **État de mal réfractaire** | ⚠ Alerte |
| Post-critique | Surveillance & Réévaluation | Manuel |

### 🎯 Prédiction IA

- Jauge de risque 0-24h avec code couleur (vert/jaune/orange/rouge)
- **Facteurs contributifs pondérés** : sommeil, observance, stress, EEG pré-ictal, alcool
- Historique des prédictions avec validation
- Recalcul temps réel

### 🩺 Tableau de bord clinique

- **Charts** — fréquence des crises, amplitude EEG, taux plasmatiques, distribution des types
- **Scores** — Glasgow, STESS, EEG ictal, étiologie
- **Thérapie** — recommandations 1ère/2ème/3ème ligne, contre-indications, grossesse
- **Calendrier RCP** interactif
- **Modules éducatifs** avec corrélations statistiques (r = 0.72 sommeil, r = -0.35 activité)

### ⌚ Intégration wearables

- EEG portable, montre connectée, smartphone, capteur de sommeil
- Statuts temps réel (online / warn / offline)
- Alertes et limites documentées

### 📹 Téléconsultation RCP (WebRTC)

- Flux vidéo local via `getUserMedia`
- 3 pairs distants simulés
- Contrôles micro / caméra / partage d'écran / enregistrement
- Latence et statut peers affichés

---

## 🏗️ `architecture`

```
┌─────────────────────────────────────────────────────────────┐
│                     EPI-SEQUENCE PRO                        │
│                                                             │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │   brain.glb  │  │ manifest.json│  │   draco/     │      │
│  │  (10 Mo)     │  │  (437 struct)│  │  (décodeur)  │      │
│  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘      │
│         │                 │                 │              │
│         └─────────────────┼─────────────────┘              │
│                           ▼                                │
│              ┌─────────────────────────┐                   │
│              │    Three.js 0.160.0     │                   │
│              │  ┌───────────────────┐  │                   │
│              │  │  GLTFLoader       │  │                   │
│              │  │  DRACOLoader      │  │                   │
│              │  │  OrbitControls    │  │                   │
│              │  │  Raycaster        │  │                   │
│              │  └───────────────────┘  │                   │
│              └───────────┬─────────────┘                   │
│                          ▼                                 │
│              ┌─────────────────────────┐                   │
│              │    Scene 3D + HUD       │                   │
│              │  ┌───────────────────┐  │                   │
│              │  │  563 meshes       │  │                   │
│              │  │  309 épileptiques │  │                   │
│              │  │  Arcs électriques │  │                   │
│              │  └───────────────────┘  │                   │
│              └───────────┬─────────────┘                   │
│                          ▼                                 │
│              ┌─────────────────────────┐                   │
│              │    Canvas WebGL         │                   │
│              └─────────────────────────┘                   │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🚀 `quick_start`

### Prérequis

- **Python 3.7+** (serveur HTTP local)
- **Navigateur moderne** (Chrome, Firefox, Edge, Safari)
- **Connexion Internet** (première fois, pour les CDN)

### Installation

```bash
# 1. Cloner le dépôt
git clone https://github.com/gunout/epi-sequence.git
cd epi-sequence

# 2. Vérifier les fichiers requis
ls -la
# Doit afficher : index.html, brain.glb, manifest.json, draco/

# 3. Lancer le serveur local
python3 -m http.server 8080
```

### Accès

Ouvre ton navigateur sur : **http://localhost:8080/**

**Identifiants de test** :
- **Utilisateur** : `dr.lefebvre@aphp.fr` (pré-rempli)
- **Mot de passe** : n'importe lequel
- **2FA** : 6 chiffres aléatoires (clique 2× sur "Se Connecter")

### Alternative : ouverture directe

```bash
open index.html      # macOS
start index.html     # Windows
xdg-open index.html  # Linux
```

> ⚠️ Pour WebRTC (`getUserMedia`), un serveur HTTP est **obligatoire**.

---

## 🎮 `controls`

### Souris

| Action | Effet |
|--------|-------|
| **Clic gauche + glisser** | Rotation 360° du cerveau |
| **Molette** | Zoom (4.5 → 15) |
| **Clic droit + glisser** | Pan (monter/descendre/déplacer) |
| **Survol** | Identifier une structure anatomique |

### Clavier

| Touche | Effet |
|--------|-------|
| `↑` / `↓` | Monter / descendre le cerveau |
| `←` / `→` | Déplacer gauche / droite |
| `Z` / `Q` / `S` / `D` | Alternative WASD |

### Boutons

| Bouton | Fonction |
|--------|----------|
| 🌐 3D | Vue 3D par défaut |
| ⬛ Axial | Vue par le dessus |
| ▭ Coronal | Vue de face |
| ▯ Sagittal | Vue de côté |
| 🔍 Rayons X | Cortex transparent |
| ↺ Reset | Réinitialiser la vue |

---

## 📁 `structure`

```
epi-sequence/
├── index.html          # Application complète (HTML + CSS + JS, ~2500 lignes)
├── brain.glb           # Cerveau 3D Draco-compressé (~10 Mo)
├── manifest.json       # Métadonnées des 437 structures anatomiques
├── LICENSE             # Licence MIT
├── README.md           # Ce fichier
│
└── draco/              # Décodeur Draco (obligatoire)
    ├── draco_decoder.js
    ├── draco_decoder.wasm
    └── draco_wasm_wrapper.js
```

---

## 🛠️ `tech_stack`

<p align="center">
  <img src="https://img.shields.io/badge/Three.js-0.160.0-FF2D95?style=for-the-badge&logo=three.js&logoColor=white" />
  <img src="https://img.shields.io/badge/WebGL-2.0-FF69B4?style=for-the-badge&logo=webgl&logoColor=white" />
  <img src="https://img.shields.io/badge/Chart.js-4.4.0-FFB6D9?style=for-the-badge&logo=chart.js&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-ES2022-FF2D95?style=for-the-badge&logo=javascript&logoColor=white" />
  <img src="https://img.shields.io/badge/HTML5-FF69B4?style=for-the-badge&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-FFB6D9?style=for-the-badge&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/WebRTC-FF2D95?style=for-the-badge&logo=webrtc&logoColor=white" />
</p>

| Composant | Technologie |
|-----------|-------------|
| **Rendu 3D** | Three.js 0.160.0 |
| **Chargement GLB** | GLTFLoader + DRACOLoader |
| **Caméra** | OrbitControls |
| **Graphiques** | Chart.js 4.4.0 |
| **Style** | CSS Vanilla (cyberpunk médical) |
| **Logique** | JavaScript ES2022 (modules) |
| **WebRTC** | API native `getUserMedia` / `getDisplayMedia` |

**Aucune étape de build** — fichier HTML autonome.

---

## 📊 `metrics`

| Métrique | Valeur |
|----------|--------|
| Structures anatomiques | **437** |
| Meshes 3D | **563** |
| Taux de match manifest | **99.3%** (559/563) |
| Meshes épileptiques | **309** |
| Arcs simultanés max | **100** |
| Taille du GLB | **~10 Mo** |
| Temps de chargement | **~3-5 s** |
| FPS moyen | **~60** (normal) / **~30** (Rayons X) |
| Mémoire navigateur | **~150 Mo** |

---

## 📈 `github_stats`

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=gunout&theme=radical&mode=daily&hide_border=true&stroke=FF2D95&background=0D001A&ring=FF69B4&fire=FF2D95&currStreakLabel=FFB6D9" alt="streak graph"/>
</p>

<p align="center">
  <img src="https://github-stats-extended.vercel.app/api/?username=gunout&show_icons=true&theme=radical&rank_icon=github&include_all_commits=true&disable_animations=true&number_format=long&show=prs_merged_percentage,prs_reviewed&hide_border=true&bg_color=0D001A&title_color=FF2D95&text_color=FFB6D9&icon_color=FF69B4" alt="stats"/>
</p>

---

## 🗺️ `roadmap`

- [x] **v9.4** — Pan vertical + clavier + 360° + Rayons X
- [ ] **v9.5** — Export GLB modifié
- [ ] **v9.6** — Mode VR (WebXR)
- [ ] **v9.7** — Multi-utilisateurs WebRTC réel
- [ ] **v10.0** — Backend FastAPI + PostgreSQL + persistance

---

## 🤝 `contribution`

```bash
# 1. Fork le projet
# 2. Créer une branche
git checkout -b feature/ma-fonctionnalite

# 3. Commit
git commit -m "feat: ajout de ma fonctionnalité"

# 4. Push
git push origin feature/ma-fonctionnalite

# 5. Ouvrir une Pull Request
```

### Convention de commit

| Préfixe | Usage |
|---------|-------|
| `feat:` | Nouvelle fonctionnalité |
| `fix:` | Correction de bug |
| `docs:` | Documentation |
| `style:` | Formatage |
| `refactor:` | Refactoring |
| `perf:` | Performance |
| `test:` | Tests |

---

## 🔐 `licenses`

### Modèle 3D

Le cerveau anatomique (`brain.glb`) et ses métadonnées (`manifest.json`) proviennent du projet **Brain Project** d'**Itay Inbar** :

- **Modèle 3D** : [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- **Code source** : [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0)
- **Dépôt** : [github.com/itayinbarr/brainproject](https://github.com/itayinbarr/brainproject)
- **Site** : [neuro.wiki/3d](https://neuro.wiki/3d)

> **Attribution obligatoire** : Le crédit `Brain model © Itay Inbar — CC BY-SA 4.0` est affiché dans l'interface.

### Bibliothèques

| Bibliothèque | Licence |
|--------------|---------|
| Three.js | MIT |
| Chart.js | MIT |
| GLTFLoader | MIT |
| DRACOLoader | Apache 2.0 |

### Ce projet

Distribué sous licence **MIT**. Voir [LICENSE](https://github.com/gunout/epi-sequence/blob/main/LICENSE).

---

## ⚠️ `avertissement_médical`

**EPI-SEQUENCE PRO est un outil de simulation et de visualisation.**

Il **ne remplace pas** :
- ❌ Un diagnostic médical
- ❌ Un protocole clinique officiel
- ❌ L'avis d'un neurologue ou urgentiste

Les données affichées (prédictions, scores, recommandations) sont **simulées** à des fins pédagogiques et de démonstration.

**En cas de crise réelle, appelez le 15 (SAMU) ou le 112.**

---

## 🐛 `troubleshooting`

| Erreur | Cause | Solution |
|--------|-------|----------|
| `brain.glb introuvable` | Fichier absent | Vérifier `ls brain.glb` |
| `No DRACOLoader instance` | Draco mal configuré | Vérifier `draco/` et `setDecoderPath('draco/')` |
| `[MANIFEST] 0 nœuds` | JSON mal formé | Vérifier `{ nodes: [...] }` |
| Page blanche | Ouvert en `file://` | Utiliser `python3 -m http.server 8080` |
| Cerveau invisible | Éclairage ou scale | Vérifier `toneMappingExposure: 0.85` et `scale = 5.5 / maxDim` |
| Arcs absents | `epilepticMeshes` vide | Vérifier les logs `[ARCS] X meshes` |

---

<p align="center">
  <img src="https://raw.githubusercontent.com/gunout/gunout/main/assets/images/divider_neon.svg" alt="Divider" />
</p>

<div align="center">

**[⬆ Retour en haut](#-epi-sequence-pro)**

[![GitHub](https://img.shields.io/badge/GitHub-gunout-FF2D95?style=for-the-badge&logo=github&logoColor=white)](https://github.com/gunout)

Fait avec ❤️ et 🧠 en France — Octobre 2026

<sub>⚡ Neon Protocol Online ⚡</sub>

</div>

<p align="center">
  <img src="https://raw.githubusercontent.com/gunout/gunout/main/assets/images/divider_neon.svg" alt="Divider" />
</p>
