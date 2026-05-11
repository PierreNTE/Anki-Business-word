# Business English Pro · SaaS · Cloud · AI

> **100 termes Business English pour francophones visant un poste**
> **Customer Success Manager · Account Executive · SaaS Sales · AI / Cloud Sales**

Application web premium, gamifiée, prête à l'emploi — un seul fichier `index.html`.
Audio natif (Web Speech API), 5 modes de jeu, répétition espacée, et export Anki en un clic.

---

## 🚀 Démarrage rapide

```
# 1. Double-cliquez sur index.html (Chrome / Edge / Safari recommandés)
# OU servez-le localement pour de meilleures voix audio :
npx serve .
```

C'est tout. Aucune installation, aucune dépendance, aucun backend.
Toute la progression (XP, niveau, série, répétition espacée, mots faibles) est sauvegardée dans `localStorage`.

---

## 📦 Contenu

| Fichier | Description |
|---|---|
| `index.html` | App premium gamifiée — 100 termes, 5 modes, exports intégrés |
| `vocabulary.json` | Dataset canonique (100 entrées × 13 champs) |
| `README.md` | Ce fichier |
| `cloud_ai_vocab_game.html` | Version originale minimaliste (conservée pour référence) |

---

## 🎓 Le dataset (100 termes)

Chaque entrée contient **13 champs** rigoureusement vérifiés :

| Champ | Description | Exemple |
|---|---|---|
| `en` | English term | `Churn` |
| `fr` | Traduction française naturelle | `Attrition / Résiliation` |
| `type` | noun · verb · expression · adjective · phrasal verb | `noun` |
| `lvl` | CEFR — A2 / B1 / B2 | `B2` |
| `cat` | Sales · Customer Success · Cloud · AI · Metrics · Legal · Negotiation · Meetings | `Customer Success` |
| `tags` | Liste de tags fonctionnels | `["customer-success","metrics"]` |
| `exp` | Définition courte en anglais simple | `When customers cancel or stop paying.` |
| `ex` | Phrase d'exemple professionnelle réaliste | `Reducing churn is our top priority...` |
| `ex2` | Phrase contextualisée SaaS / AI | `A 5% monthly churn rate will destroy ARR...` |
| `ipa` | Prononciation IPA | `/tʃɜːrn/` |
| `tip` | Conseil de prononciation pour francophones | `Son « tch » initial comme dans "church"` |
| `syn` | Synonymes professionnels courants | `["attrition","cancellation"]` |
| `err` | Erreur typique d'un francophone | `"Churn out" signifie produire en masse...` |
| `mem` | Astuce mnémotechnique | `Penser à la baratte qui agite le lait...` |
| `alts` | Réponses françaises alternatives acceptées | `["attrition","résiliation","resiliation"]` |

### Couverture par catégorie

- **Sales** — Pipeline, Forecast, Quota, MEDDIC, BANT, Business case, Close plan, Cold outreach…
- **Customer Success** — Churn, Renewal, Onboarding, Health score, QBR, Time-to-value, Customer journey…
- **Cloud** — SaaS, PaaS, IaaS, Cloud-native, Multi-cloud, Kubernetes, Serverless, Managed services…
- **AI** — LLM, GenAI, RAG, Fine-tuning, Inference, Hallucination, AI agent, Foundation model…
- **Metrics** — ARR, MRR, NRR, ACV, CAC, LTV, TCO, ROI, NPS, Retention…
- **Legal** — SLA, MSA, SOW, NDA, Compliance, Data sovereignty…
- **Meetings / Negotiation** — Touch base, Loop in, Circle back, Reach out, Objection handling…

---

## 🎮 Modes de jeu

| Mode | Description | XP gagné |
|---|---|---|
| 🎴 **Flashcards** | Flip carte EN → FR avec exemples enrichis | +10 |
| ⇢ **EN → FR** | Tape la traduction française du terme anglais | +15 |
| ⇠ **FR → EN** | Tape le terme anglais (B2 → fluency) | +15 |
| 🎧 **Listening** | Écoute (Normal / Slow) et tape ce que tu entends | +15 |
| ⏱ **Timed** | 30 s par carte — pression réelle de l'entretien | +15 |

Filtres : **Catégorie** + **Niveau CEFR**. Sessions de 20 cartes priorisées par la répétition espacée (Leitner 5 boîtes).

### Système de correction strict mais juste

- ✅ Accepte les variantes sans accents (`resiliation` ≈ `résiliation`)
- ✅ Accepte la ponctuation manquante et la casse différente
- ✅ Accepte les synonymes français pré-validés (champ `alts`)
- ❌ **Ne valide jamais** une réponse anglaise grammaticalement fausse
- 🧠 Affiche systématiquement : la bonne réponse + ton entrée + tip + erreur typique + mnémonique

### Gamification

- **XP & Niveau** (formule `level = 1 + √(xp/40)`)
- **Streak quotidien** 🔥 (incrémenté chaque jour consécutif d'usage)
- **Répétition espacée** (Leitner : 4 h → 1 j → 3 j → 7 j → 14 j)
- **Tableau « weak words »** (les 15 termes les plus ratés)
- **Stats dashboard** (Accuracy, Mastered count, Sessions)
- **Sound effects** via Web Speech API (Slow mode pour francophones)

### Raccourcis clavier

| Touche | Action |
|---|---|
| `Space` | Retourner / passer à la suivante |
| `Enter` | Valider la réponse |
| `Tab` | Révéler la bonne réponse |
| `←` / `→` | Carte précédente / suivante |
| `P` | Prononcer le terme courant |
| `S` | Ouvrir les statistiques |
| `E` | Ouvrir le panneau d'export |
| `Esc` | Fermer la modale |

---

## 🃏 Import dans Anki

1. Dans l'app, cliquez sur **⬇** (top bar) → **🃏 Anki TSV**
2. Téléchargez `business-english-anki.tsv`
3. Ouvrez Anki → **Fichier → Importer** → sélectionnez le fichier
4. Type de note : **Basic** · Field 1 → Front · Field 2 → Back · Field 3 → Tags
5. Cochez **« Allow HTML in fields »**
6. Importer ✓

Le deck Anki produit inclut :
- **Recto** : terme, IPA, catégorie, niveau, type
- **Verso** : traduction FR, définition EN, deux exemples, tip prononciation, erreur typique, mnémo, synonymes
- **Tags** : `level_B2`, `cat_sales`, `customer-success`, etc.

---

## 📤 Autres exports

| Format | Usage |
|---|---|
| **CSV** | Excel · Google Sheets · Notion · Quizlet |
| **JSON** | Réutilisation programmatique, autres apps |
| **Markdown** | Dictionnaire imprimable, Obsidian, blog perso |
| **Anki TSV** | Import Anki direct avec HTML formatté |

Tous générés côté client — aucune donnée n'est envoyée à un serveur.

---

## 🎯 Plan d'apprentissage suggéré (30 jours)

| Phase | Durée | Objectif |
|---|---|---|
| 1. **Découverte** | J1 → J3 | Flashcards uniquement · toutes catégories · niveau A2/B1 |
| 2. **Production** | J4 → J10 | EN → FR · catégorie ciblée par jour (Sales / CS / Cloud / AI) |
| 3. **Inversion** | J11 → J18 | FR → EN · révèle les vrais trous |
| 4. **Compréhension orale** | J19 → J24 | Listening · Slow mode au début, puis Normal |
| 5. **Pression entretien** | J25 → J30 | Timed mode 30s · niveau B2 uniquement |

Objectif raisonnable : **20–30 min/jour**, streak quotidien maintenu.
Cible avant entretien : **80%+ d'accuracy en Timed B2**.

---

## 🧪 Qualité linguistique

Toutes les phrases d'exemple ont été rédigées pour sonner **natif**, comme dans de vraies réunions B2B :

- ✅ Anglais SaaS moderne (« crush quota », « land and expand », « slip to next quarter »)
- ✅ Pas de buzzwords démodés (« synergy », « blue-sky thinking »)
- ✅ Traductions FR validées pour le contexte business français
- ✅ Erreurs courantes des francophones ciblées (« forecast » mal prononcé, confusion `close /kloʊz/` vs `/kloʊs/`)

---

## 🔒 Vie privée

- 100% client-side. Aucun tracking, aucun envoi serveur.
- `localStorage` uniquement (clé `bep_state_v1`). Effaçable depuis Stats → Reset.
- L'audio utilise les voix locales du navigateur (Web Speech API). Pas d'appel API externe.

---

## 🛠 Stack technique

| Couche | Choix |
|---|---|
| Front | HTML5 + CSS3 (variables, grid) + JavaScript (vanilla, zéro dépendance) |
| Audio | Web Speech API (`speechSynthesis`) — voix natives du système |
| Persistance | `localStorage` (Leitner SRS + XP + stats) |
| Design | Inspiré Linear / Notion / Stripe / Vercel · gamification façon Duolingo |
| Theming | Dark mode par défaut + Light mode (toggle 🌓) |
| Responsive | Mobile-first, breakpoint 640 px |
| Accessibilité | ARIA labels, focus visible, `prefers-reduced-motion`-friendly |

### Pourquoi pas React/Next.js ?

L'app tient en un seul fichier (~80 ko), démarre instantanément, fonctionne hors ligne dès le premier chargement, sans build ni install. C'est parfait pour de l'apprentissage quotidien. Le dataset `vocabulary.json` reste exportable vers n'importe quel stack moderne (React, Vue, Svelte, Next.js…).

---

## 🚀 Pour passer à Next.js plus tard

```bash
npx create-next-app@latest business-english-pro --typescript --tailwind --app
# Copier vocabulary.json dans /data
# Réutiliser la logique de buildDeck(), srsRecord(), buildAnkiTSV() telle quelle
```

---

## 📝 Licence & contribution

Usage personnel libre. Pour ajouter des termes, éditez le tableau `VOCAB` dans `index.html` (ou `vocabulary.json` puis collez-le inline). Le système supporte n'importe quel nombre d'entrées.

---

**Bon entraînement. Crush your interview. 🚀**
