# solution-accessoires.fr — consignes pour les agents

Site statique (GitHub Pages, domaine `solution-accessoires.fr`) de Solution Accessoires,
boutique Solution Phone au 21 rue Gambetta, 71000 Mâcon. Tout le texte est en français, au vouvoiement.

## Fichiers
- `index.html` : accueil (rayons d'accessoires, hydrogel, stock des reconditionnés, garantie, boutique).
- `hydrogel.html` : page protection écran hydrogel (5 formules).
- `404.html` : page introuvable.
- `catalogue.js` : catalogue des accessoires (généré, ne pas modifier à la main).
- `menu-commun.js` : menu commun aux 3 sites — fichier IDENTIQUE sur les 3 dépôts, ne pas le modifier ici.
  Le bloc `#mc-footer` en bas de chaque page (liens statiques) fait partie du menu commun.
- `plan-acces.js` : plan Google Maps chargé seulement au clic (« Voir le plan »).
- `boutique.css` (commun), `accueil.css` (accueil). Augmenter `?v=` après modification.

## Faits à respecter (source unique)
- Téléphone Solution Accessoires : 06 02 84 99 53 ; WhatsApp : 07 83 92 18 84 ; e-mail : contact@solution-phone.fr.
- Horaires : mardi à samedi 10h–12h / 14h–19h, fermé dimanche et lundi.
- Note Google : « 5,0/5 · 20 avis Google ». Pas d'aggregateRating en JSON-LD.
- Reconditionnés : contrôlés sur 30 points, garantis 12 mois, mis de côté 48 h ; transfert de données dès 20 €.
- Hydrogel : Saphir 10 €, Privacy Onyx 10 €, Crystal 20 €, Obsidian Privacy 20 €, ECOSHIELD 7H 30 €, pose incluse ;
  pas de garantie, sauf défaut du produit (6 mois).
- Paiement : carte, espèces (1 000 € maximum), Apple Pay, virement ; pas de chèque ni de paiement en plusieurs fois.
- « Une boutique Solution Phone » (jamais « partenaire » ni « indépendante ») ; « depuis 2014 ».
- QualiRépar : « labellisé », jamais « certifié » ni « l'État finance ».

## Stock (reconditionnés)
- Lecture seule des tables Supabase `phones` et `phones_neufs` (requêtes dans `loadStock`, à garder telles quelles).
- Les noms sont normalisés à l'affichage seulement (règles de solution-phone.fr/reconditionnes-v2.js).
- Aucun téléphone de démonstration : si la base ne répond pas, message « Stock momentanément indisponible ».

## Vérifier
`python3 -m http.server 4193` puis tester en 375 px et en bureau : 0 erreur console, pas de défilement horizontal,
JSON-LD valide.
