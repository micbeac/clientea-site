# Klientea — déploiement du site sur Vercel

Site statique (1 fichier `index.html` + `og-image.png`). Aucune compétence technique requise.

## Contenu du dossier
- `index.html` — la landing page complète.
- `og-image.png` — l'image affichée quand le lien est partagé sur les réseaux / WhatsApp / Google.
- `README-deploiement.md` — ce guide.

## 1. Mettre le site en ligne sur Vercel (méthode la plus simple)

1. Crée un compte gratuit sur https://vercel.com (connexion avec Google/GitHub possible).
2. Sur le dashboard, clique **Add New… → Project**.
3. Choisis l'option d'import par glisser-déposer : **Deploy a folder** (ou installe l'app et fais glisser le dossier `site-clientea`).
   - Alternative propre : mets le dossier dans un dépôt **GitHub**, puis « Import » ce dépôt dans Vercel. Chaque modification se redéploie toute seule.
4. Laisse les réglages par défaut (framework = « Other / Static »), clique **Deploy**.
5. En ~30 s, ton site est en ligne sur une adresse `xxxx.vercel.app`.

## 2. Brancher le domaine klientea.com

1. Achète **klientea.com** (chez Vercel : onglet **Domains**, ou chez un registrar comme OVH/Namecheap).
2. Dans le projet Vercel → **Settings → Domains → Add** → tape `klientea.com`.
3. Suis les instructions DNS affichées (si acheté ailleurs, copie les enregistrements indiqués chez ton registrar). Vercel gère le HTTPS automatiquement.

## 3. Activer le formulaire « Réserver une démo »

Le formulaire fonctionne déjà en mode secours (il ouvre un e-mail pré-rempli). Pour recevoir les demandes directement dans ta boîte mail, branche **Web3Forms** (gratuit) :

1. Va sur https://web3forms.com → entre ton e-mail → tu reçois une **Access Key**.
2. Ouvre `index.html`, cherche `VOTRE_CLE_WEB3FORMS` et remplace-le par ta clé.
3. Redéploie (ou re-glisse le dossier). Les demandes arriveront par e-mail.

> Remplace aussi l'adresse `contact@klientea.com` (dans `index.html`, pied de page + formulaire) par ton vraie adresse tant que l'e-mail du domaine n'est pas créé.

## 4. À personnaliser avant de communiquer dessus
- Adresse e-mail de contact (2 endroits dans `index.html`).
- La clé Web3Forms (point 3).
- Optionnel : un vrai numéro de téléphone si tu veux ajouter un bouton « Appelez-nous ».

## Bon à savoir
- Le texte, les couleurs et les sections se modifient directement dans `index.html`.
- L'image sociale (`og-image.png`) doit rester accessible à l'adresse `https://klientea.com/og-image.png` pour s'afficher dans les partages.
