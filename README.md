# Créer un jeu sur minisjeux.hastag.fr

Merci de vouloir contribuer ! Voici la marche à suivre, étape par étape.

## 1. Forker ce dépôt

En haut à droite de la page GitHub de ce dépôt → bouton **Fork**. Ça crée une copie du dépôt sur ton propre compte, sur laquelle tu as tous les droits.

## 2. Cloner ton fork et créer une branche

```bash
git clone https://github.com/TON-PSEUDO/minisjeux-submissions.git
cd minisjeux-submissions
git checkout new-games
git checkout -b mon-jeu
```

Remplace `mon-jeu` par un nom qui te parle — le nom de la branche n'a pas besoin d'être identique à l'identifiant final du jeu.

## 3. Ajouter ton jeu

Place un unique fichier **`index.html`** à la racine de ta branche. Contraintes techniques :

- **Un seul fichier** : tout le HTML, le CSS et le JavaScript doivent être dans ce `index.html` (pas de fichiers séparés, pas de dossier `assets/`)
- **Taille max : 2 Mo**
- Le fichier doit contenir au moins une balise `<script>` — un jeu sans JavaScript ne passera pas la vérification automatique
- Pas de dépendances externes qui nécessitent un service payant
- Pense au mobile si tu coches la case correspondante dans la Pull Request : le jeu doit être jouable au toucher, pas seulement au clavier/souris

## 4. Tester en local

Ouvre simplement ton `index.html` dans un navigateur pour vérifier que tout fonctionne avant de proposer ta Pull Request — ça évite un aller-retour inutile avec la vérification automatique.

## 5. Pousser ta branche et ouvrir la PR

```bash
git add index.html
git commit -m "Ajout de mon jeu"
git push origin mon-jeu
```

Sur GitHub, une bannière "Compare & pull request" doit apparaître → clique dessus.

**Important** : vérifie que la PR cible bien `new-games` comme branche de base (pas `main`).

## 6. Remplir le formulaire de la PR

Un template se pré-remplit automatiquement dans le corps de la PR. Remplis chaque champ :

- **Nom** : le nom affiché du jeu
- **Emoji** : un seul emoji représentatif du jeu
- **Description** : une ou deux phrases qui donnent envie d'y jouer
- **Compatible mobile** : coche seulement si tu as vraiment testé sur téléphone/tablette
- **C'est un jeu à score** : coche si le jeu a un système de points
- **Score excellent** : uniquement si tu as coché la case au-dessus — un score que tu juges comme un "bon score" à atteindre, pour donner un repère aux joueurs. Laisse vide sinon.

## 7. La suite est automatique

Une fois ta PR ouverte :

1. Un bot vérifie automatiquement la structure de ta soumission (quelques secondes)
2. Si tout est bon, ta PR passe en attente de relecture par un modérateur
3. Un modérateur relit ton code et peut te demander des ajustements — réponds directement sur la PR, pousse de nouveaux commits sur ta branche si besoin, la vérification se relance toute seule
4. Une fois ton code approuvé, un modérateur déclenche la publication — ton jeu apparaît alors automatiquement sur le site, et ta PR se ferme d'elle-même juste après. **Cette fermeture n'est pas un rejet** : c'est la confirmation que ton jeu est en ligne.

## Questions

Ouvre une issue sur ce dépôt si un point n'est pas clair, ou pose la question directement en commentaire sur ta PR.
