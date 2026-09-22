# 🏝️ Octroi de Mer — DROM

Dashboard interactif d'analyse des tarifs d'octroi de mer pour les **4 DROM français**.

[![License: MIT](https://img.shields.io/badge/License-MIT-0055A4.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26.svg?logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/HTML)
[![Plotly](https://img.shields.io/badge/Plotly-2.27-3F4F75.svg?logo=plotly&logoColor=white)](https://plotly.com/javascript/)
[![Produits](https://img.shields.io/badge/Produits-38_809-EF4135.svg)]()

---

## 🎯 Présentation

Ce dépôt héberge un **dashboard web interactif** pour explorer **38 809 produits tarifaires** soumis à l'octroi de mer dans les DROM.

| Territoire | Produits | Taux moyen | Taux max |
|:---|:---:|---:|---:|
| 🇫🇷 Guadeloupe | 9 664 | 8,70 % | 50,00 % |
| 🇫🇷 Martinique | 18 996 | 9,78 % | 50,00 % |
| 🇫🇷 La Réunion | 531 | 6,61 % | 61,50 % |
| 🇫🇷 Guyane | 9 617 | 2,48 % | 28,50 % |
| **Total** | **38 809** | | |

> ⚠️ L'octroi de mer ne concerne que les **5 DROM**. Les COM (Polynésie, Nouvelle-Calédonie, Wallis-et-Futuna, Saint-Pierre-et-Miquelon, Saint-Barthélemy, Saint-Martin) ont des fiscalités autonomes.

---

## 🚀 Démo en ligne

👉 **[https://gunout.github.io/octroi-drom/](https://gunout.github.io/octroi-drom/)**

### Activation GitHub Pages

1. **Settings** → **Pages**
2. **Source** : `Deploy from a branch`
3. **Branch** : `main` / `root`
4. **Save**

---

## 📁 Structure du dépôt

- `README.md` — Documentation (ce fichier)
- `LICENSE` — Licence MIT
- `index.html` — Dashboard interactif (~40 Ko)
- `data/dashboard_data.json` — Données consolidées (~15 Mo)

---

## 💻 Installation locale

Cloner le dépôt :

    git clone https://github.com/gunout/octroi-drom.git
    cd octroi-drom
    python3 -m http.server 8000

Puis ouvrir dans le navigateur :

    http://localhost:8000/

> ⚠️ Un serveur HTTP est **obligatoire** — l'ouverture directe via `file://` ne fonctionne pas (blocage CORS du navigateur).

---

## ⚡ Fonctionnalités

- **5 onglets** : Vue d'ensemble · Comparaison · Chapitres SH · Recherche · Simulateur
- **4 KPI cards** : produits, taux moyen, taux max, chapitres SH
- **Recherche instantanée** par code SH ou libellé
- **Simulateur** d'octroi par territoire
- **Export** CSV · JSON · PNG
- **Thème** clair / sombre
- **Design tricolore** 🇫🇷

---

## 📊 Structure des données

Le fichier `data/dashboard_data.json` contient :

- `total_produits` : 38809
- `stats_par_territoire` : statistiques par DROM
- `produits` : tableau des 38 809 produits

Chaque produit possède les champs suivants :

- `territoire` — Ex : GUADELOUPE
- `code_nc` — Code nomenclature combinée (ex : 2009 89 97)
- `chapitre` — Chapitre SH (2 premiers chiffres)
- `libelle` — Description du produit
- `taux_ome` — Taux octroi de mer externe
- `taux_omre` — Taux octroi de mer régional externe
- `annexe` — Catégorie A / B / C

### Signification des taux

| Code | Signification |
|:---|:---|
| **OME** | Octroi de Mer Externe (importations) |
| **OMRE** | Octroi de Mer Régional Externe (taux réduit) |
| **OMI** | Octroi de Mer Interne (livraisons locales) |
| **OMRI** | Octroi de Mer Régional Interne (taux réduit) |

---

## 📚 Sources officielles

- [Data Économie](https://data.economie.gouv.fr/explore/dataset/octroi-de-mer-dans-les-departements-doutre-mer/) — Tarifs DROM
- [Douane française](https://www.douane.gouv.fr/la-douane/opendata) — Tarifs officiels
- [Cour des comptes](https://www.ccomptes.fr) — Rapport 2024
- [Légifrance](https://www.legifrance.gouv.fr) — Délibérations

---

## 🤝 Contribuer

1. **Fork** le projet
2. Créer une branche : `git checkout -b feature/ma-fonctionnalite`
3. Commit : `git commit -m "feat: ma fonctionnalité"`
4. Push : `git push origin feature/ma-fonctionnalite`
5. Ouvrir une **Pull Request**

| Préfixe | Signification |
|:---|:---|
| `feat:` | Nouvelle fonctionnalité |
| `fix:` | Correction |
| `docs:` | Documentation |
| `style:` | Formatage |
| `refactor:` | Refactoring |
| `chore:` | Maintenance |

---

## 🗺️ Roadmap

- [x] Dashboard interactif (Plotly)
- [x] 38 809 produits · 4 DROM
- [x] Recherche + Simulateur
- [x] Export CSV / JSON / PNG
- [x] Thème sombre + tricolore 🇫🇷
- [ ] Ajout de Mayotte (OCR)
- [ ] API REST Flask
- [ ] Comparateur temporel

---
<div align="center">
## 📄 Licence

[MIT](LICENSE) © 2026 [gunout](https://github.com/gunout)
</div>

---

<div align="center">

**🇫🇷 Fait avec ❤️ pour les DROM 🇫🇷**

⭐ N'hésitez pas à mettre une étoile si ce projet vous est utile !

</div>


---

<div align="center">

### 🇫🇷 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>Gunout</strong> — Tous droits réservés.</sub>

</div>
