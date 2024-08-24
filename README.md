# Chasseur de Primes Maladroit

## Description
"Chasseur de Primes Maladroit" est un jeu de tir développé en HTML, CSS et JavaScript pur. Le joueur incarne un chasseur de primes maladroit qui doit capturer différentes cibles mouvantes avant qu'elles ne s'échappent.

## Fonctionnalités principales
- Plusieurs types de cibles avec des comportements différents
- Système de vies pour le joueur et les cibles
- Décompte visuel du temps restant pour capturer une cible
- Système de score basé sur l'argent gagné
- Difficulté progressive
- Messages humoristiques pour les succès et les échecs
- Statistiques de jeu en temps réel
- Écran de fin de partie avec récapitulatif des performances

## Règles du jeu

### Objectif
Capturer autant de cibles que possible avant de perdre toutes vos vies.

### Déroulement
1. Une cible apparaît à l'écran avec 3 vies.
2. Le joueur doit cliquer sur la cible pour lui faire perdre ses vies.
3. Chaque clic réussi rapporte de l'argent au joueur.
4. Si la cible perd toutes ses vies, elle est capturée et une nouvelle cible apparaît.
5. Si le temps imparti s'écoule avant la capture, la cible s'échappe et le joueur perd une vie.

### Système de points
- 1 point pour un clic normal
- 2 points pour un clic rapide (entre 1 et 2 secondes)
- 3 points pour un clic très rapide (moins d'1 seconde)

### Difficulté progressive
Le temps alloué pour capturer une cible diminue progressivement :
- 30 secondes : de 0 à 10 cibles capturées
- 25 secondes : de 11 à 20 cibles
- 20 secondes : de 21 à 30 cibles
- 15 secondes : de 31 à 50 cibles
- 12 secondes : à partir de 51 cibles

### Fin de partie
La partie se termine lorsque le joueur perd ses 3 vies. Un écran récapitulatif affiche alors les performances du joueur.

## Fonctionnement technique

### Structure du projet
Le jeu est contenu dans un seul fichier HTML qui inclut le CSS et le JavaScript.

### Technologies utilisées
- HTML5
- CSS3
- JavaScript (ES6+)

### Composants principaux

1. **Zone de jeu** : Un conteneur div où les cibles apparaissent et se déplacent.
2. **Cibles** : Représentées par des emojis avec des comportements de mouvement uniques.
3. **Viseur** : Un élément SVG qui suit le mouvement de la souris.
4. **Timer** : Une barre de progression et un décompte numérique pour le temps restant.
5. **Affichage des statistiques** : Zones de texte mises à jour en temps réel.

### Fonctions clés

- `changeTarget()` : Génère une nouvelle cible et initialise ses propriétés.
- `moveTarget()` : Déplace la cible de manière aléatoire dans la zone de jeu.
- `updateTimer()` : Met à jour le temps restant et change la couleur du décompte.
- `handleCapture()` : Gère la logique lorsqu'une cible est entièrement capturée.
- `targetEscaped()` : Gère la logique lorsqu'une cible s'échappe.
- `getAllocatedTime()` : Détermine le temps alloué en fonction du nombre de captures.

### Gestion des événements
- Événement 'mousemove' pour le mouvement du viseur.
- Événement 'click' pour la détection des clics sur les cibles.

### Optimisations
- Utilisation de `requestAnimationFrame` pour des animations fluides.
- Gestion efficace de la mémoire en réutilisant les objets cibles.

## Installation et exécution
1. Clonez ce dépôt sur votre machine locale.
2. Ouvrez le fichier `index.html` dans un navigateur web moderne.
3. Le jeu devrait démarrer automatiquement.

## Compatibilité
Ce jeu est conçu pour fonctionner sur les navigateurs web modernes supportant HTML5, CSS3 et ES6+.

## Contributions
Les contributions sont les bienvenues ! N'hésitez pas à forker le projet, créer une branche, ajouter vos modifications et soumettre une pull request.

## Licence
Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.
