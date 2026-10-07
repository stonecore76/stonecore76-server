# StoneCore76 — boutique / précommande

Site complet de démonstration avec catalogue, panier, paiement Stripe Checkout, acompte 50 %, paiement 100 %, commandes, suivi colis, espace client, tickets service client et tableau de bord admin.

## Lancer sur Windows
1. Installer Node.js LTS.
2. Ouvrir un terminal dans ce dossier.
3. `npm install`
4. Copier `.env.example` vers `.env`.
5. Renseigner les clés Stripe.
6. `npm start`
7. Ouvrir http://localhost:3000

Compte admin de démonstration : admin@stonecore76.fr / ChangeMe123! — à changer avant production.

## Stripe
Le site utilise Stripe Checkout : les cartes bancaires ne sont pas stockées par StoneCore76. Pour un compte Stripe si tu es mineur, utilise les informations et la représentation légale exigées par Stripe avec ton parent/représentant légal. Ne mets jamais une clé secrète Stripe dans le dossier `public`.

Webhook : `POST /api/stripe/webhook`.

## Fonctionnement 50/50
Le client choisit 50 % ou 100 %. Après le premier paiement, l'admin peut créer un lien de solde depuis le tableau de bord. Quand le solde est payé, la commande peut être expédiée.

## Suivi
L'admin renseigne le transporteur et le numéro de suivi. Le client le voit dans son espace personnel et peut ouvrir le suivi transporteur.

## Production
Configurer HTTPS, clés Stripe LIVE, webhook Stripe de production, secret de session aléatoire, vrai compte admin, sauvegardes de base et obligations commerciales applicables en France. Le ZIP est le code du site : il doit encore être déployé et configuré pour devenir un site public.
