# 🔑 Information Clé API Mistral

## Clé API Configurée

Votre clé API Mistral est **intégrée dans le fichier .skill** pour fonctionner sur Claude.ai.

**Clé** : `k6OZYgiKhV...W5P4` (masquée pour sécurité)

---

## ⚠️ Sécurité Importante

### Ce Fichier Contient Votre Clé API

Le fichier `french-invoice-analyzer.skill` contient votre clé API Mistral dans `config.yaml`.

**C'est normal et nécessaire** pour que le skill fonctionne sur Claude.ai, mais :

❌ **NE PAS** partager publiquement le fichier .skill
❌ **NE PAS** uploader sur GitHub public
❌ **NE PAS** envoyer par email non chiffré

✅ **UNIQUEMENT** uploader sur votre compte Claude.ai personnel
✅ **UNIQUEMENT** utiliser pour votre usage personnel

---

## 🔄 Si Vous Voulez Partager le Skill

Si vous voulez partager ce skill avec d'autres :

### Option 1 : Version sans clé
```bash
# Utiliser la version: french-invoice-analyzer-NO-KEY.skill
# Les utilisateurs devront configurer leur propre clé
```

### Option 2 : Régénérer une version propre
1. Éditer `config.yaml` dans le skill
2. Remplacer par : `# api_key: "your_mistral_api_key"`
3. Re-zipper le skill
4. Les utilisateurs utiliseront leur propre clé

---

## 💰 Gestion de la Clé

### Surveiller l'Usage

Allez sur https://console.mistral.ai pour :
- Voir votre consommation
- Définir des limites de dépense
- Créer d'autres clés si nécessaire

### Révoquer la Clé

Si la clé est compromise :
1. Allez sur https://console.mistral.ai
2. Settings > API Keys
3. Révocquez l'ancienne clé
4. Créez une nouvelle clé
5. Mettez à jour `config.yaml` dans le skill

---

## 📊 Coûts Estimés

Avec Mistral OCR :
- 10 factures : ~$0.01 (1 centime)
- 100 factures : ~$0.10 (10 centimes)
- 1000 factures : ~$1.00 (1 dollar)

**Très économique !**

---

## ✅ Résumé

- ✅ Clé API configurée dans le skill
- ✅ Prêt pour upload sur Claude.ai
- ✅ .gitignore protège les fichiers locaux
- ⚠️  Ne pas partager le .skill publiquement (contient la clé)

**Le skill est prêt à l'emploi !**
