<div align="center">

# 🧠 EPI-SEQUENCE PRO

**Interface médicale 3D interactive pour la simulation de crises épileptiques**

[![Version](https://img.shields.io/badge/version-9.4.0-00e5ff?style=flat-square)](https://github.com/gunout/epi-sequence)
[![Three.js](https://img.shields.io/badge/Three.js-0.160.0-a855f7?style=flat-square&logo=three.js&logoColor=white)](https://threejs.org/)
[![License](https://img.shields.io/badge/license-MIT-00ff9d?style=flat-square)](https://github.com/gunout/epi-sequence/blob/main/LICENSE)
[![Status](https://img.shields.io/badge/status-active-00ff9d?style=flat-square)](https://github.com/gunout/epi-sequence)
[![Stars](https://img.shields.io/github/stars/gunout/epi-sequence?style=flat-square&color=00e5ff)](https://github.com/gunout/epi-sequence/stargazers)
[![Forks](https://img.shields.io/github/forks/gunout/epi-sequence?style=flat-square&color=a855f7)](https://github.com/gunout/epi-sequence/network)
[![Issues](https://img.shields.io/github/issues/gunout/epi-sequence?style=flat-square&color=ff3b6b)](https://github.com/gunout/epi-sequence/issues)
[![Last Commit](https://img.shields.io/github/last-commit/gunout/epi-sequence?style=flat-square&color=ffd93b)](https://github.com/gunout/epi-sequence/commits)
[![Code Size](https://img.shields.io/github/languages/code-size/gunout/epi-sequence?style=flat-square&color=ff8b3b)](https://github.com/gunout/epi-sequence)
[![Made with Love](https://img.shields.io/badge/made%20with-%E2%9D%A4%EF%B8%8F%20%26%20%F0%9F%A7%A0-ff3b6b?style=flat-square)](https://github.com/gunout/epi-sequence)

</div>

---

## 📋 Aperçu

**EPI-SEQUENCE PRO** est une interface web médicale immersive qui combine :

- 🧠 **Atlas cérébral 3D** — 437 structures, 563 meshes (source : Brain Project d'Itay Inbar)
- ⚡ **Arcs électriques rouges** ancrés sur les structures corticales
- 📊 **Séquenceur CTAG** — protocole d'état de mal épileptique (0-60 min)
- 🎯 **Prédiction IA** — risque de crise à 24h
- 🩺 **HUD clinique complet** — scores Glasgow, STESS, EEG, RCP Live

> ⚠️ **Démonstration technologique** — Ne constitue pas un dispositif médical certifié.

---

## 🚀 Lancement rapide

Ouvre un terminal et exécute :

```bash
git clone https://github.com/gunout/epi-sequence.git
cd epi-sequence
python3 -m http.server 8080
```

Ouvre ensuite **http://localhost:8080/** dans ton navigateur.

**Identifiants** : `dr.lefebvre@aphp.fr` / mot de passe libre / 2FA : 6 chiffres.

---

## ✨ Fonctionnalités

| 3D | Médical | UI |
|---|---|---|
| Rotation 360° | Séquenceur CTAG | Login 4 rôles |
| Zoom limité (4.5→15) | 4 phases SE | 4 dossiers patients |
| Pan vertical | Prédiction 24h | 8 onglets |
| 4 vues (3D/Axial/Coronal/Sagittal) | Scores Glasgow/STESS | Charts Chart.js |
| Mode Rayons X | Recommandations thérapeutiques | RCP Live WebRTC |
| Couleurs anatomiques | Calendrier RCP | Feedback IA |
| Survol interactif | Modules éducatifs | Snapshots PNG |

---

## 🎮 Contrôles

| Action | Souris | Clavier |
|--------|--------|---------|
| Rotation | Clic gauche + glisser | — |
| Zoom | Molette | — |
| Pan | Clic droit + glisser | Flèches ↑↓←→ |
| Alternative | — | Z/Q/S/D |

---

## 📁 Structure

```
epi-sequence/
├── index.html          # Application complète (~2500 lignes)
├── brain.glb           # Cerveau 3D Draco-compressé (~10 Mo)
├── manifest.json       # 437 structures anatomiques
├── draco/              # Décodeur Draco
│   ├── draco_decoder.js
│   ├── draco_decoder.wasm
│   └── draco_wasm_wrapper.js
├── LICENSE             # MIT
└── README.md
```

---

## 🏗️ Stack

| Composant | Technologie |
|-----------|-------------|
| Rendu 3D | Three.js 0.160.0 |
| GLB + Draco | GLTFLoader + DRACOLoader |
| Caméra | OrbitControls |
| Graphiques | Chart.js 4.4.0 |
| Style | CSS Vanilla (cyberpunk médical) |
| Logique | JavaScript ES2022 |
| WebRTC | API native |

**Aucune étape de build** — fichier HTML autonome.

---

## 📊 Métriques

| Métrique | Valeur |
|----------|--------|
| Structures anatomiques | 437 |
| Meshes 3D | 563 |
| Taux de match manifest | 99.3% |
| Meshes épileptiques | 309 |
| Arcs simultanés max | 100 |
| FPS moyen | ~60 (normal) / ~30 (Rayons X) |

---

## 🔐 Licences et crédits

**Modèle 3D** — [Brain Project](https://github.com/itayinbarr/brainproject) d'Itay Inbar
- Modèle : [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- Code source : Apache 2.0
- Site : [neuro.wiki/3d](https://neuro.wiki/3d)

> Crédit obligatoire : `Brain model © Itay Inbar — CC BY-SA 4.0` (affiché dans l'interface)

**Bibliothèques** : Three.js (MIT), Chart.js (MIT), GLTFLoader (MIT), DRACOLoader (Apache 2.0).

**Projet** : MIT — voir [LICENSE](https://github.com/gunout/epi-sequence/blob/main/LICENSE).

---

## ⚠️ Avertissement médical

**EPI-SEQUENCE PRO est un outil de simulation et de visualisation.**

Il **ne remplace pas** un diagnostic médical, un protocole clinique officiel, ou l'avis d'un neurologue. Les données affichées sont **simulées** à des fins pédagogiques.

**En cas de crise réelle, appelez le 15 (SAMU) ou le 112.**

---

## 🐛 Problèmes fréquents

| Erreur | Solution |
|--------|----------|
| `brain.glb introuvable` | Vérifier `ls brain.glb` |
| `No DRACOLoader instance` | Vérifier `draco/` et `setDecoderPath('draco/')` |
| `[MANIFEST] 0 nœuds` | Vérifier `{ nodes: [...] }` dans le JSON |
| Page blanche | Ne pas ouvrir en `file://`, utiliser un serveur HTTP |
| Cerveau invisible | Vérifier `toneMappingExposure: 0.85` |

---

## 🗺️ Roadmap

- [x] v9.4 — Pan vertical + clavier
- [ ] v9.5 — Export GLB modifié
- [ ] v9.6 — Mode VR (WebXR)
- [ ] v9.7 — Multi-utilisateurs WebRTC réel
- [ ] v10.0 — Backend (FastAPI + PostgreSQL)

---

## 🤝 Contribution

```bash
git checkout -b feature/ma-fonctionnalite
git commit -m "feat: ajout de X"
git push origin feature/ma-fonctionnalite
```

Puis ouvrir une **Pull Request** sur GitHub.

**Convention** : `feat:` / `fix:` / `docs:` / `style:` / `refactor:` / `test:`

---

## 📞 Contact

- **Auteur** : [@gunout](https://github.com/gunout)
- **Projet** : [github.com/gunout/epi-sequence](https://github.com/gunout/epi-sequence)

---

<div align="center">

**[⬆ Retour en haut](#-epi-sequence-pro)**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/gunout/epi-sequence)

Fait avec ❤️ et 🧠 en France — Octobre 2026

</div>
