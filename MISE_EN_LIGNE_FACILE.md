# Mettre votre site en ligne en 15 minutes
## Guide simplifié pour le Dr Uriel Drassouline

Ce guide est pensé pour quelqu'un qui n'a **aucune compétence technique**. Pas de jargon, pas de code à écrire. Juste des étapes claires.

---

## Ce dont vous avez besoin

- Votre ordinateur avec accès internet
- Une carte bancaire (pour acheter le nom de domaine, ~15 €)
- 15 minutes de temps calme

---

## ÉTAPE 1 — Acheter votre adresse web (5 minutes, ~15 €)

### 1.1 — Ouvrez votre navigateur et allez sur :
**https://www.ovh.com/fr/domaines/**

### 1.2 — Dans la grande barre de recherche, tapez :
```
laserriviera-nice.fr
```

### 1.3 — Cliquez sur le bouton **« Rechercher »**

### 1.4 — Deux cas possibles :
- **Si c'est vert** « Disponible » → super, cliquez sur **« Commander »**
- **Si c'est rouge** « Déjà pris » → essayez dans l'ordre : `laserriviera.fr`, puis `clinique-laser-riviera.fr`, puis `laser-riviera-nice.fr`

### 1.5 — Créez un compte OVH
- Email
- Mot de passe
- Vos coordonnées

### 1.6 — Payez par carte bleue
- Le prix : ~12 à 15 € pour 1 an
- Cochez « renouvellement automatique » (évite de perdre le domaine par oubli)

### 1.7 — Gardez bien votre email et mot de passe OVH
Vous en aurez besoin à l'étape 3.

**✅ Vous êtes propriétaire de laserriviera-nice.fr !**

---

## ÉTAPE 2 — Mettre le site en ligne GRATUITEMENT (5 minutes)

### 2.1 — Ouvrez un nouvel onglet et allez sur :
**https://app.netlify.com/signup**

### 2.2 — Créez un compte gratuit
- Le plus simple : cliquez sur **« Sign up with Google »** si vous utilisez déjà Gmail
- Sinon : email + mot de passe

### 2.3 — Une fois connecté, cherchez le gros bouton :
**« Add new site »** → cliquez dessus
**« Deploy manually »** (= déployer manuellement) → cliquez dessus

### 2.4 — Une page s'ouvre avec une grande zone vide qui dit :
*« Drag and drop your site folder here »*

### 2.5 — Sur votre ordinateur :
- Allez dans le dossier où se trouve **SITE_CENTRE_LASER** (dans votre dossier DEVIS cr)
- **Glissez le dossier SITE_CENTRE_LASER complet** vers cette zone Netlify dans votre navigateur
- Lâchez la souris

### 2.6 — Attendez 30 secondes
Netlify vous affiche **« Your site is live »** avec une adresse bizarre comme `https://superbe-chat-12345.netlify.app`

### 2.7 — Cliquez sur cette adresse pour vérifier que votre site s'affiche bien !

**✅ Votre site est en ligne ! Mais pas encore sur laserriviera-nice.fr.**

---

## ÉTAPE 3 — Connecter votre vraie adresse à Netlify (5 minutes)

### 3.1 — Sur Netlify, dans votre site, cliquez sur :
**« Domain settings »** (à gauche dans le menu)

### 3.2 — Cliquez sur le bouton :
**« Add custom domain »**

### 3.3 — Entrez votre adresse achetée à l'étape 1 :
```
laserriviera-nice.fr
```
Puis cliquez **« Verify »** puis **« Add domain »**.

### 3.4 — Netlify vous affiche des instructions DNS
Ça ressemble à ça :
```
Point your domain to: 75.2.60.5
Or use Netlify's DNS servers:
- dns1.p01.nsone.net
- dns2.p01.nsone.net
...
```

**🎯 GARDEZ CETTE PAGE OUVERTE, vous allez en avoir besoin.**

### 3.5 — Ouvrez un nouvel onglet et allez sur :
**https://www.ovh.com/manager/**

### 3.6 — Connectez-vous avec votre compte OVH (créé à l'étape 1)

### 3.7 — Dans le menu à gauche, cliquez sur **« Web Cloud »**, puis **« Noms de domaine »**

### 3.8 — Cliquez sur **laserriviera-nice.fr**

### 3.9 — Dans l'onglet **« Serveurs DNS »**, cliquez sur **« Modifier les serveurs DNS »**

### 3.10 — Remplacez les serveurs DNS par ceux que Netlify vous a donnés :
```
dns1.p01.nsone.net
dns2.p02.nsone.net
dns3.p03.nsone.net
dns4.p04.nsone.net
```
(Les valeurs exactes sont celles que Netlify vous a affichées à l'étape 3.4)

### 3.11 — Cliquez **« Confirmer »**

### 3.12 — Patientez entre 30 minutes et 24 heures
C'est le temps que la modification se propage sur internet (normal).

### 3.13 — Après ce délai, tapez dans votre navigateur :
```
https://laserriviera-nice.fr
```
**Votre site s'affiche avec le petit cadenas vert 🔒 ! Vous êtes en ligne.**

---

## 🚨 SI VOUS ÊTES PERDU : l'alternative « clé en main »

Si à n'importe quel moment vous bloquez, voici deux solutions alternatives :

### Option A — Faire appel à un développeur freelance
- Aller sur **Malt** (https://www.malt.fr) ou **Fiverr** (https://www.fiverr.com)
- Rechercher : **« Mise en ligne site HTML Netlify + domaine OVH »**
- Tarif : 80 à 150 € pour tout faire à votre place
- Durée : 1 à 2 h de son côté

### Option B — Appeler le support OVH
- Numéro : **1007** (depuis un mobile français) ou **09 72 10 10 07**
- Dire : *« Bonjour, je suis débutant, j'ai acheté un nom de domaine et je voudrais connecter mon site hébergé sur Netlify. Pouvez-vous me guider ? »*
- Le support OVH est français et patient.

---

## APRÈS la mise en ligne : les choses à faire

### 1. Déclarer votre site sur Google (10 min — très important pour le SEO)
- Aller sur **https://search.google.com/search-console**
- Se connecter avec un compte Google
- Ajouter **laserriviera-nice.fr**
- Cela permet à Google de découvrir et indexer votre site

### 2. Créer votre fiche Google Business Profile (20 min — essentiel)
- Aller sur **https://www.google.com/business/**
- Créer une fiche « Clinique Laser de la Riviera »
- Adresse : 31 rue Meyerbeer 06000 Nice
- Catégorie : Centre d'épilation au laser
- Photos (au moins 10) du cabinet et du matériel
- C'est **le levier SEO local le plus puissant** pour capter des patients à Nice

### 3. Mettre 3-4 vrais avis Google dans la zone « Avis »
Dites-moi si vous voulez, je vous formate ça.

### 4. Faire relire les mentions légales par un avocat (~150 €)
Je peux vous rédiger les 3 pages légales obligatoires (mentions légales, politique de confidentialité, cookies) pour que l'avocat n'ait plus qu'à relire.

---

## Résumé ultra-court (à imprimer)

1. **OVH** → acheter `laserriviera-nice.fr` (~15 €)
2. **Netlify** → créer compte gratuit → glisser le dossier SITE_CENTRE_LASER → site en ligne
3. **Netlify Domain Settings** → ajouter `laserriviera-nice.fr` → copier les serveurs DNS
4. **OVH → Noms de domaine → DNS** → coller les serveurs DNS de Netlify
5. Attendre quelques heures → votre site est en ligne avec votre vraie adresse.

---

## Contactez-moi à tout moment

Si vous bloquez sur une étape, dites-moi :
- À quelle étape vous êtes
- Ce que vous voyez à l'écran (une capture d'écran aide énormément)

Et je vous guide exactement sur la suite.
