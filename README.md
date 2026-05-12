# Business English Pro · SaaS · Cloud · AI

> **125 termes Business English pour francophones visant un poste**
> **Customer Success Manager · Account Executive · SaaS Sales · AI / Cloud Sales**

Application web premium, gamifiée, prête à l'emploi — publiée sur GitHub Pages et installable sur mobile.
Audio natif (Web Speech API), choix d'accent US/UK, 5 modes de jeu, répétition espacée, et export Anki en un clic.

---

## 🚀 Démarrage rapide

Version en ligne : [https://pierrente.github.io/Anki-Business-word/](https://pierrente.github.io/Anki-Business-word/)

Sur téléphone, ouvrez ce lien dans Chrome ou Safari, puis ajoutez l'app à l'écran d'accueil.

```bash
# 1. Double-cliquez sur index.html (Chrome / Edge / Safari recommandés)
# OU servez-le localement pour de meilleures voix audio :
python -m http.server 4173
# puis ouvrez http://127.0.0.1:4173/
```

C'est tout. Aucune installation, aucune dépendance, aucun backend.
Toute la progression (XP, niveau, série, répétition espacée, mots faibles) est sauvegardée dans `localStorage`, appareil par appareil.

---

## 📱 Installation mobile / PWA

L'app inclut un `manifest.webmanifest`, un service worker et des icônes pour être installée comme une application.

### Android

1. Ouvrir [https://pierrente.github.io/Anki-Business-word/](https://pierrente.github.io/Anki-Business-word/) dans Chrome.
2. Menu `⋮` → **Ajouter à l'écran d'accueil**.
3. Lancer l'app depuis l'icône **English Pro**.

### iPhone / iPad

1. Ouvrir l'URL dans Safari.
2. Bouton **Partager** → **Sur l'écran d'accueil**.
3. Lancer l'app depuis l'icône.

Si une ancienne version reste affichée, fermez l'app complètement puis rouvrez-la. Le service worker met le cache à jour automatiquement après publication.

---

## 📦 Contenu

| Fichier | Description |
| --- | --- |
| `index.html` | App premium gamifiée — 125 termes, 5 modes, exports intégrés |
| `vocabulary.json` | Dataset canonique (125 entrées × 15 champs) |
| `manifest.webmanifest` | Métadonnées PWA pour installation mobile |
| `sw.js` | Service worker : cache offline + mise à jour PWA |
| `icon-192.png` / `icon-512.png` | Icônes mobile / PWA |
| `README.md` | Ce fichier |
| `cloud_ai_vocab_game.html` | Version originale minimaliste (conservée pour référence) |

---

## 🎓 Le dataset (125 termes)

Chaque entrée contient **15 champs** rigoureusement vérifiés :

| Champ | Description | Exemple |
| --- | --- | --- |
| `en` | English term | `Churn` |
| `fr` | Traduction française naturelle | `Attrition / Résiliation` |
| `type` | noun · verb · expression · adjective · adverb · phrasal verb | `noun` |
| `cat` | Sales · Customer Success · Cloud · AI · Metrics · Legal · Negotiation · Meetings · Expressions | `Customer Success` |
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
- **Expressions** — Adjectifs & adverbes business (tremendous, robust, seamless, granular, significantly, ultimately…), idiomes (to sum up, at the end of the day, low-hanging fruit, move the needle…)

---

## 🎮 Modes de jeu

| Mode | Description | XP gagné |
| --- | --- | --- |
| 🎴 **Flashcards** | Recto anglais → bouton **Voir la réponse** → verso traduction + auto-évaluation | +10 |
| ⇢ **EN → FR** | Tape la traduction française du terme anglais | +15 |
| ⇠ **FR → EN** | Tape le terme anglais (production active) | +15 |
| 🎧 **Listening** | Écoute US/UK (Normal / Slow), choisis une voix anglaise, puis tape ce que tu entends | +15 |
| ⏱ **Timed** | 30 s par carte — pression réelle de l'entretien | +15 |

Filtre : **Catégorie** (Sales, Customer Success, Cloud, AI, Metrics, Legal, Negotiation, Meetings, Expressions). Sessions de 20 cartes priorisées par la répétition espacée (Leitner 5 boîtes).

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
- **Audio Web Speech API** avec choix **US / UK**, menu de voix anglaises disponibles et bouton **Tester la voix**

### Audio et accents

Le mode Listening utilise les voix disponibles dans le navigateur ou le système.

- Choix rapide : **US** ou **UK**.
- Menu **Voix** : sélection manuelle d'une voix anglaise précise (`Google US English`, `Microsoft Aria`, `Samantha`, `Google UK English`, etc.).
- Bouton **Tester la voix** pour comparer rapidement les options.
- Les voix non anglaises sont ignorées pour éviter une prononciation trop française.

Si aucune voix anglaise n'apparaît, installez une voix **English US** ou **English UK** dans les paramètres système, ou testez dans Chrome / Edge.

### Raccourcis clavier

| Touche | Action |
| --- | --- |
| `Space` | Révéler la flashcard / passer à la suivante selon le mode |
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

- **Recto** : terme, IPA, catégorie, type
- **Verso** : traduction FR, définition EN, deux exemples, tip prononciation, erreur typique, mnémo, synonymes
- **Tags** : `cat_sales`, `cat_expressions`, `customer-success`, etc.

### Style premium dans Anki

L'app fournit aussi un bouton **🎨 Style Anki premium (CSS + template)** dans le panneau d'export.

Procédure :

1. Dans Anki Desktop → **Parcourir** → cliquez une carte du deck.
2. Bouton **Cartes…** → onglet **Styling**.
3. Dans l'app web → **⬇** → **🎨 Style Anki premium** → **Copier le CSS Anki**.
4. Collez le CSS dans **Styling**.
5. Utilisez `{{Front}}` pour le recto et `{{FrontSide}}<hr id="answer">{{Back}}` pour le verso.
6. Synchronisez Anki : le style suit sur mobile.

---

## 📤 Autres exports

| Format | Usage |
| --- | --- |
| **CSV** | Excel · Google Sheets · Notion · Quizlet |
| **JSON** | Réutilisation programmatique, autres apps |
| **Markdown** | Dictionnaire imprimable, Obsidian, blog perso |
| **Anki TSV** | Import Anki direct avec HTML formatté |

Tous générés côté client — aucune donnée n'est envoyée à un serveur.

---

## 🎯 Plan d'apprentissage suggéré (30 jours)

| Phase | Durée | Objectif |
| --- | --- | --- |
| 1. **Découverte** | J1 → J3 | Flashcards uniquement · toutes catégories |
| 2. **Production** | J4 → J10 | EN → FR · catégorie ciblée par jour (Sales / CS / Cloud / AI) |
| 3. **Inversion** | J11 → J18 | FR → EN · révèle les vrais trous |
| 4. **Compréhension orale** | J19 → J24 | Listening · Slow mode au début, puis Normal |
| 5. **Pression entretien** | J25 → J30 | Timed mode 30s · toutes catégories |

Objectif raisonnable : **20–30 min/jour**, streak quotidien maintenu.
Cible avant entretien : **80%+ d'accuracy en Timed**.

---

## 🧪 Qualité linguistique

Toutes les phrases d'exemple ont été rédigées pour sonner **natif**, comme dans de vraies réunions B2B :

- ✅ Anglais SaaS moderne (« crush quota », « land and expand », « slip into next quarter »)
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
| --- | --- |
| Front | HTML5 + CSS3 (variables, grid) + JavaScript (vanilla, zéro dépendance) |
| Audio | Web Speech API (`speechSynthesis`) — accent US/UK + sélection de voix anglaise |
| Persistance | `localStorage` (Leitner SRS + XP + stats) |
| PWA | `manifest.webmanifest` + `sw.js` + icônes PNG |
| Design | Inspiré Linear / Notion / Stripe / Vercel · gamification façon Duolingo |
| Theming | Dark mode par défaut + Light mode (toggle 🌓) |
| Responsive | Mobile-first, breakpoint 640 px |
| Accessibilité | ARIA labels, focus visible, `prefers-reduced-motion`-friendly |

### Pourquoi pas React/Next.js ?

Le coeur de l'app tient dans `index.html`, démarre instantanément et ne demande aucun build. Les fichiers PWA ajoutent seulement l'installation mobile, les icônes et le cache offline. C'est parfait pour de l'apprentissage quotidien. Le dataset `vocabulary.json` reste exportable vers n'importe quel stack moderne (React, Vue, Svelte, Next.js…).

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

Bon entraînement. Crush your interview. 🚀
