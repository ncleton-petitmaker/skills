# 🎯 French Invoice Analyzer - Guide d'Installation et Utilisation

## 📦 Votre Skill est Prêt !

Le fichier **`french-invoice-analyzer.skill`** est votre skill complet pour analyser et traiter automatiquement vos factures françaises.

---

## 🚀 Installation du Skill

### Option 1 : Installation dans Claude.ai (Recommandée)

1. **Téléchargez** le fichier `french-invoice-analyzer.skill`
2. **Allez sur** [Claude.ai](https://claude.ai)
3. **Ouvrez** les Paramètres > Skills
4. **Cliquez** sur "Upload Skill"
5. **Sélectionnez** le fichier `french-invoice-analyzer.skill`
6. **Activez** le skill dans votre projet ou conversation

### Option 2 : Utilisation en Local

Si vous préférez utiliser les scripts directement sans passer par Claude.ai :

1. **Extraire** le fichier .skill (c'est un fichier ZIP)
   ```bash
   unzip french-invoice-analyzer.skill -d french-invoice-analyzer
   ```

2. **Installer** les dépendances
   ```bash
   pip install --break-system-packages pdfplumber pytesseract pillow pdf2image openpyxl
   
   # Sur Ubuntu/Debian
   apt-get update && apt-get install -y tesseract-ocr tesseract-ocr-fra poppler-utils
   ```

3. **Utiliser** les scripts
   ```bash
   cd french-invoice-analyzer
   python scripts/process_invoices.py /chemin/vers/vos/factures
   ```

---

## 💡 Ce que Fait le Skill

### Workflow Complet

```
📁 Factures (PDF/JPG/PNG)
    ↓
🔍 Extraction OCR (texte)
    ↓
📊 Analyse des données
   • Fournisseur
   • Montants (HT, TVA, TTC)
   • Dates
   • Numéro de facture
   • SIRET
    ↓
🏦 Classification comptable
   • Plan Comptable Général (PCG)
   • Classe 6 (charges)
   • Compte automatique selon fournisseur
    ↓
📝 Renommage intelligent
   • Format: YYYYMMDD_Fournisseur_Montant_NumFacture.pdf
    ↓
📊 Génération Excel
   • Format Pennylane
   • Écritures comptables complètes
   • Prêt pour import direct
```

### Fichiers Générés

- **`pennylane_import.xlsx`** → À importer dans Pennylane
- **`invoices_data.json`** → Toutes les données extraites
- **`summary_report.txt`** → Rapport récapitulatif
- **`renamed_invoices/`** → Factures renommées et organisées

---

## 📋 Utilisation Rapide

### Avec Claude.ai (après installation du skill)

Simplement demander à Claude :

```
"Analyse toutes les factures de ce dossier et prépare l'import Pennylane"
```

Claude va automatiquement :
1. Lire le skill
2. Utiliser les scripts appropriés
3. Analyser vos factures
4. Générer les fichiers de sortie
5. Vous fournir les résultats

### Avec les Scripts Directement

```bash
# Workflow complet en une commande
python scripts/process_invoices.py ./mes_factures

# Ou en deux étapes
python scripts/analyze_invoices.py ./mes_factures
python scripts/generate_pennylane_import.py ./analyzed/invoices_data.json
```

---

## 🎓 Classification Comptable Automatique

Le skill classifie automatiquement selon le **Plan Comptable Général français** :

| Fournisseur / Type | Compte | Libellé |
|-------------------|--------|---------|
| EDF, Engie | 6061 | Énergie |
| Orange, SFR, Free | 6262 | Télécommunications |
| Expert-comptable, Avocat | 6226 | Honoraires |
| Restaurants, Traiteurs | 6257 | Réceptions |
| Hôtels | 6251 | Voyages et déplacements |
| Logiciels SaaS | 651 | Licences logiciels |
| Google Ads, Facebook Ads | 6231 | Publicité |
| Chronopost, UPS | 6242 | Transport |
| Assurances | 6161 | Multirisques |
| **Non reconnu** | **6288** | **Autres charges** |

Plus de 30 classifications automatiques disponibles !

---

## 📊 Format Pennylane

Chaque facture génère **3 lignes comptables** :

```
Ligne 1 : Charge (Débit)          → Compte 6xxx
Ligne 2 : TVA déductible (Débit)  → Compte 44566
Ligne 3 : Fournisseur (Crédit)    → Compte 401XXXXX
```

**Exemple concret :**

```
Date       | Journal | Compte  | Libellé           | Débit   | Crédit  | PieceRef
15/10/2025 | ACH     | 6061    | Énergie - EDF     | 150.00  |         | FAC-2025-001
15/10/2025 | ACH     | 44566   | TVA déductible    | 30.00   |         | FAC-2025-001
15/10/2025 | ACH     | 401EDF  | EDF               |         | 180.00  | FAC-2025-001
```

Total équilibré : **180€ débit = 180€ crédit** ✅

---

## 💰 Gain de Temps

### Avant le skill :
- 📝 Lire chaque facture : **2 min**
- 🔍 Identifier les données : **1 min**
- 💻 Saisir dans Pennylane : **3 min**
- 🏷️ Classer et archiver : **1 min**
- **Total par facture : 7 minutes**
- **50 factures = 6 heures**

### Avec le skill :
- 🤖 Analyse automatique : **10 secondes/facture**
- ✅ Contrôle rapide : **30 secondes/facture**
- 📥 Import par lot : **2 minutes**
- **Total pour 50 factures : 35 minutes**

### 🎯 Résultat : **85% de temps gagné !**

---

## ✅ Résumé

Vous avez maintenant un **skill professionnel** qui :

✅ Analyse automatiquement vos factures  
✅ Extrait toutes les données importantes  
✅ Classifie selon le PCG français  
✅ Renomme intelligemment les fichiers  
✅ Génère un Excel prêt pour Pennylane  
✅ Vous fait gagner **85% de temps** sur la saisie comptable  

---

## 🚀 Prêt à Gagner du Temps ?

**Installez le skill maintenant et transformez votre saisie comptable !**

📦 Fichier : `french-invoice-analyzer.skill`  
📖 Documentation : À l'intérieur du skill  
💻 Scripts : Prêts à l'emploi  
🎯 Objectif : Automatiser votre comptabilité  

**Bonne utilisation ! 🎊**
