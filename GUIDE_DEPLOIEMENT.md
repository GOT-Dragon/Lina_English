# 📱 App Anglais pour la Fille - Guide de Déploiement

## 📋 Fichiers créés

- ✅ **index.html** - Application complète
- ✅ **manifest.json** - Configuration PWA (theme color en rose #e91e63)
- ✅ **sw.js** - Service Worker avec cache
- ✅ **icon192.png** - Icône 192x192 (recadrée de la photo)
- ✅ **icon512.png** - Icône 512x512 (recadrée de la photo)

## 🚀 Déploiement sur GitHub Pages

### Option 1 : Créer un dossier `/daughter/` dans ton repo

1. Crée un nouveau dossier `daughter` à la racine de ton repo `got-dragon.github.io`
2. Place tous les fichiers ci-dessus dans ce dossier
3. Push vers GitHub
4. L'app sera accessible à : **https://got-dragon.github.io/daughter/**

Commandes Git :
```bash
mkdir daughter
cd daughter
# Copie les fichiers ici
git add -A
git commit -m "Add daughter English app"
git push
```

### Option 2 : Utiliser une URL personnalisée (sous-domaine)

Si tu veux une URL comme `daughter.got-dragon.github.io`, il faudrait un repo séparé.

## 📊 Changements par rapport à la version de Charly

### Vocab
- ✅ Dico **vide au départ** - ta fille l'alimente avec ses mots
- ✅ Mots usuels pour enfants choisis à l'ouverture (35 mots comme : apple, cat, dog, etc.)
- ✅ Icône = photo de ta fille recadrée (rose/rose foncé)

### Oral
- ✅ **Seul l'onglet "Dialogue"** (l'onglet "Écrit" a été supprimé)
- ✅ 3 dialogues simples pour enfants prédéfinis
- ✅ Phonétique incluse pour chaque ligne

### Quiz
- ✅ Fonctionne seulement avec les mots ajoutés par ta fille
- ✅ Alimenté par les mots usuels pour l'ouverture du app

### Autres
- ❌ Phrases Pro = supprimées
- ✅ Traducteur = gardé tel quel
- 🎨 Couleur thème = rose/magenta (#e91e63) au lieu de bleu

## 🔄 Synchronisation Supabase

**User ID séparé :** `got_dragon_daughter`

L'app utilise :
- Même compte Supabase (même URL et clé)
- Mais un **user ID différent**, donc les données sont complètement séparées
- Résultat : deux collections indépendantes dans la même table

Si tu veux désactiver la sync cloud (mode local seulement), tu peux :
1. Ouvrir `index.html` dans un éditeur
2. Chercher les lignes : `const sbUrl = ...` et `const sbKey = ...`
3. Les laisser vides pour un mode local-only

## 📱 Installation sur téléphone

- iOS : Ouvre le lien → Partage → Ajouter à l'écran d'accueil
- Android : Menu (⋮) → Installer l'application

L'icône rose avec la photo de ta fille apparaîtra sur l'écran d'accueil !

## 🎯 Prochaines étapes possibles

1. **Partager avec d'autres enfants ?** → Change juste le user ID Supabase
2. **Ajouter des dialogues ?** → Modifie le tableau `DIALOGS` dans `index.html`
3. **Changer les mots usuels ?** → Modifie le tableau `COMMON_WORDS` dans `index.html`
4. **Ajouter une section "Écrit" ?** → Je peux la réajouter sur demande

---

**Créé le :** 14 mai 2026  
**Pour :** Fille de Charly  
**Thème :** Rose/Magenta avec couronne 👑
