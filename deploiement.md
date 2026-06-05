# Guide de déploiement — Clinique Laser de la Riviera

**Site :** laserriviera-nice.fr
**Livré le :** 21 avril 2026
**Par :** Assistant SEO Dr Uriel Drassouline

---

## Étape 1 — Acheter le nom de domaine (5 min, ~12 €/an)

### Vérifier la disponibilité

Aller sur **OVH** (https://www.ovh.com/fr/domaines/) ou **Gandi** (https://www.gandi.net) et tester dans cet ordre :

1. `laserriviera-nice.fr` ← priorité 1
2. `laserriviera-nice.com`
3. `laserriviera.fr`
4. `laserriviera.com`
5. `clinique-laser-riviera.fr`

**Recommandation forte :** acheter **les deux versions (.fr ET .com)** pour empêcher un concurrent de récupérer l'autre extension. Budget total : ~25 €/an.

### Options à activer à l'achat

- **Protection Whois** (cache vos coordonnées personnelles) — gratuit chez OVH, inclus chez Gandi
- **Auto-renouvellement** activé (évite la perte accidentelle)
- **DNSSEC** activé (sécurité DNS)

---

## Étape 2 — Choisir un hébergement (15 min, ~3 à 7 €/mois)

### Option A — Simple et économique : OVH Perso

- URL : https://www.ovh.com/fr/hebergement-web/
- Prix : 3,59 €/mois
- Inclus : 100 Go stockage, certificat SSL gratuit, PHP, MySQL
- **Parfait pour ce site HTML statique.**

### Option B — Gratuit et ultra-rapide : Vercel ou Netlify (recommandé)

Si vous voulez la vitesse maximale (impact SEO positif) et zéro maintenance :

- **Netlify** : https://www.netlify.com → glisser-déposer le dossier `SITE_CENTRE_LASER`, associer le domaine. Gratuit, HTTPS automatique.
- **Vercel** : https://vercel.com → même principe.

**Avantages Vercel/Netlify** : CDN mondial, HTTPS automatique, site chargé en <1s partout dans le monde (Google adore).

---

## Étape 3 — Mettre le site en ligne (10 min)

### Via OVH (FTP classique)

1. Depuis l'espace OVH, récupérer les identifiants FTP (serveur, login, mot de passe).
2. Télécharger **FileZilla** (gratuit) : https://filezilla-project.org
3. Se connecter au FTP, uploader **le contenu** du dossier `SITE_CENTRE_LASER/` (pas le dossier lui-même) dans `/www/`.
4. Le site est accessible sur `laserriviera-nice.fr` (propagation DNS : 1 à 24 h).
5. Activer le **certificat SSL gratuit** depuis l'espace OVH (Let's Encrypt, 1 clic).

### Via Netlify / Vercel (encore plus simple)

1. Créer un compte gratuit.
2. Glisser-déposer le dossier `SITE_CENTRE_LASER/` sur la page d'accueil Netlify.
3. Le site est instantanément en ligne avec une URL temporaire `.netlify.app`.
4. Onglet « Domain settings » → ajouter `laserriviera-nice.fr`.
5. Suivre les instructions DNS (copier les enregistrements A/CNAME chez OVH).
6. HTTPS activé automatiquement en 30 minutes.

---

## Étape 4 — Compléter les éléments [À COMPLÉTER] dans le HTML (15 min)

Ouvrir `index.html` dans un éditeur de texte (VS Code, Notepad++, Sublime) et faire **Ctrl+F** sur `[À COMPLÉTER]` ou `[À compléter]`. Vous trouverez :

| N° | Emplacement | À remplir par |
|---|---|---|
| 1 | Section Médecin — nom complet | `Dr Prénom NOM` (ex : `Dr Uriel Drassouline`) |
| 2 | Section Médecin — n° RPPS | Votre numéro RPPS à 11 chiffres (**obligatoire légalement**) |
| 3 | Tableau tarifs — 8 lignes | Vos tarifs indicatifs (fourchettes acceptées : « à partir de 60 € ») |
| 4 | Avis — nombre d'avis Google | Ex : « 127 avis » |
| 5 | Avis — zone encadrée | Copier-coller 4 à 6 avis Google réels, ou installer le widget Google |
| 6 | Contact — lien Doctolib | Votre URL Doctolib (ex : `https://www.doctolib.fr/chirurgien-esthetique/nice/uriel-drassouline`) |
| 7 | Footer — Directeur de publication et RPPS | Même infos que la section médecin |

### Éléments optionnels à ajouter

- **Email professionnel** : `contact@laserriviera-nice.fr` (créer l'adresse chez OVH/Gmail Workspace)
- **Photo du médecin** : remplacer le placeholder « Dr » par une vraie photo professionnelle. Dans le code, chercher `medecin-photo-placeholder` et remplacer par `<img src="photo-medecin.jpg" alt="Dr NOM, chirurgien esthétique Nice">`
- **Logo** : créer un logo simple sur Canva (gratuit) et remplacer le SVG du favicon

---

## Étape 5 — Créer les 3 pages légales obligatoires (30 min)

**Sans ces pages, votre site est en infraction** (loi LCEN 2004-575 + RGPD + Code de la consommation).

Créer 3 fichiers à côté de `index.html` :

### `mentions-legales.html`

Contenu minimum obligatoire :
- Nom + prénom du directeur de publication (vous)
- N° RPPS + Ordre des Médecins département 06
- Adresse du cabinet
- Téléphone + email
- Hébergeur (nom + adresse, ex : « OVH SAS, 2 rue Kellermann 59100 Roubaix »)
- N° SIRET de votre structure

### `politique-confidentialite.html`

Conforme RGPD :
- Quelles données collectées (nom, email, téléphone du formulaire)
- Finalité (réponse à la demande de RDV uniquement)
- Durée de conservation (ex : 3 ans après dernier contact)
- Destinataires (vous uniquement, aucune cession tiers)
- Droits du patient (accès, rectification, effacement, opposition, portabilité) + email DPO
- Base légale (consentement + exécution précontractuelle)

### `cookies.html`

Liste des cookies utilisés :
- Cookies strictement nécessaires (aucun consentement requis)
- Cookies de mesure d'audience (Google Analytics si installé) — consentement obligatoire
- Moyen de retirer son consentement

**Astuce :** des générateurs gratuits existent (ex : https://www.cnil.fr/fr/modele/courrier) mais **faites relire par un avocat** (1 h ~ 150 €, amortie sur des années).

---

## Étape 6 — Google Search Console (obligatoire pour le SEO, 15 min)

1. Aller sur https://search.google.com/search-console
2. Cliquer « Ajouter une propriété » → choisir **Domaine** (pas URL).
3. Saisir `laserriviera-nice.fr`
4. Google donne un enregistrement TXT → le copier dans les DNS OVH (zone DNS → ajouter → TXT).
5. Attendre 10 min, cliquer « Vérifier ».
6. Une fois vérifié :
   - Aller dans **Sitemaps** → soumettre `https://laserriviera-nice.fr/sitemap.xml` (voir étape 7)
   - **Inspection d'URL** → demander l'indexation de la page d'accueil

### À surveiller chaque semaine dans Search Console

- Nombre de pages indexées (doit monter progressivement)
- Couverture : erreurs éventuelles
- Performances : requêtes qui vous apportent des clics
- Mobile usability : zéro erreur attendue avec ce code

---

## Étape 7 — Créer sitemap.xml et robots.txt (5 min)

Créer ces 2 fichiers à la racine du site, à côté de `index.html`.

### `sitemap.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://laserriviera-nice.fr/</loc>
    <lastmod>2026-04-21</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

### `robots.txt`

```
User-agent: *
Allow: /

Sitemap: https://laserriviera-nice.fr/sitemap.xml
```

---

## Étape 8 — Google Business Profile (le plus rentable à court terme, 30 min)

**Le SEO local se gagne ici avant même sur votre site web.**

1. Aller sur https://www.google.com/business/
2. Créer une fiche pour « Clinique Laser de la Riviera »
3. Catégorie principale : **Centre médical** ou **Dermatologue**
4. Catégories secondaires : **Centre d'épilation au laser**, **Clinique esthétique**
5. Remplir à 100 % : adresse, horaires, téléphone, site web (laserriviera-nice.fr), photos (10+ photos du cabinet, du matériel, de l'équipe)
6. Description : 750 caractères max, inclure les mots-clés **« laser Nice »**, **« épilation laser »**, **« détatouage »**, **« Carré d'Or »**
7. Activer la messagerie
8. Publier au moins 1 post par semaine (nouveauté, rappel saisonnier, FAQ)

### Demande d'avis patients (CNOM-compliant)

Demandez oralement à chaque patient satisfait en fin de consultation :
> « Si vous êtes satisfait, un avis Google nous aide beaucoup. Voici le lien par SMS. »

**Interdit** : offrir une remise contre avis. Les avis sollicités contre contrepartie sont sanctionnables (DGCCRF + CNOM).

---

## Étape 9 — Connecter le formulaire contact à un vrai back-end (10 min)

Le formulaire actuel est une démonstration (il ne fait qu'afficher une alerte JavaScript). Pour le rendre fonctionnel :

### Option simple : **Formspree** (gratuit jusqu'à 50 messages/mois)

1. Créer un compte sur https://formspree.io
2. Récupérer votre endpoint (ex : `https://formspree.io/f/abcdxyz`)
3. Dans `index.html`, remplacer la balise `<form class="contact-form-wrapper" onsubmit="...">` par :
   ```html
   <form class="contact-form-wrapper" action="https://formspree.io/f/VOTRE-ID" method="POST">
   ```
4. Supprimer l'attribut `onsubmit="..."`.

### Option plus avancée : **EmailJS**, **Web3Forms** ou back-end PHP

Pour volume plus élevé ou intégration CRM.

---

## Étape 10 — Mesurer et améliorer (continu)

### Installer Google Analytics 4 (consent-mode RGPD)

Guide officiel : https://support.google.com/analytics/answer/9304153

### Tester la vitesse du site

https://pagespeed.web.dev/ → score cible : **> 90/100** sur mobile.

### Tester la qualité du SEO on-page

- https://www.seobility.net/en/seocheck/ (gratuit, français supporté)
- Vérifier qu'aucune erreur rouge n'apparaît

### Checklist hebdomadaire (15 min/semaine)

- [ ] Publier 1 post Google Business Profile
- [ ] Répondre aux nouveaux avis Google (positifs ET négatifs, poliment)
- [ ] Vérifier Search Console (erreurs, nouvelles requêtes)
- [ ] Ajouter 1 à 2 photos/semaine sur Google Business
- [ ] Vérifier le formulaire de contact (recevez-vous bien les messages ?)

---

## Récapitulatif des coûts (année 1)

| Poste | Coût |
|---|---|
| 2 noms de domaine (.fr + .com) | ~25 € |
| Hébergement OVH ou équivalent | ~45 € (ou 0 € chez Vercel/Netlify) |
| Email pro (optionnel Google Workspace) | ~72 € (ou 0 € chez OVH) |
| Relecture juridique mentions légales | ~150 € (une fois) |
| **TOTAL année 1** | **~150 à 290 €** |

**Année 2 et +** : 70 à 140 € / an.

---

## Support

En cas de blocage sur n'importe quelle étape, demandez-moi directement la procédure détaillée. Je peux aussi vous rédiger :
- Les 3 pages légales conformes
- Le contenu Google Business Profile optimisé
- Les templates de SMS/email pour demander des avis
- Un guide vidéo pas-à-pas

Bonne mise en ligne !
