# But
Ce projet est une initiation faite à Télécom Paris au Machine Learning. Il s'agit de retravailler le premier réseaux de neuronnes appelé perceptron de rosenblatt. De ce fait, on se familiarise avec les concepts clés suivants de la branche de la classification : 
- Fonction de décision ; 
- Fonction de Cout et la Descente gradient.

# Démarches
L'ensemble des exercices est contenu dans le fichier perceptron.pdf. Ils se répartissent en 04 grandes parties : 
- 1_Génération des données de différentes distribution ; 
- 2_Perceptron linéaire ;
- 3_Fonction_cout ; 
- 4_Descente_gradient 

# Découvertes 
Fonction de décision
Géométriquement, c'est l'hyperplan qui sépare les classes. Elle est idéalle si elle maximise donc la distance entre les classes. Dans la pratique, il y a un chevauchement entre les points.

Algébriquement, l'hyperplan le plus simple est une droite de forme :
f(w, x) = w0 + w1 * x1
où w1 est le poids. Dans la pratique, cette forme peut avoir plusieurs variables x.

La fonction de décision peut avoir la forme de droite mais aussi d'autres formes géométriques : ellipse, parabole, etc. L'efficacité de la forme dépend de la distribution des données.

Fonction coût
Dans l'espace des données, il existe une infinité possible de fonction de décision pour une forme donnée. Pour trouver la fonction de décision optimale, c'est là qu'entre en jeu la fonction de coût et la descente gradient.

Bien qu'il y ait des variantes, la fonction coût minimise en général l'écart entre la prédiction f(w) et la valeur réelle. Chaque observation a un coût. Au lieu de minimiser tous les coûts, on minimise la fonction coût moyenne :

Pour la régression :
J(w) = (1/m) * Σ (f(w, xᶦ) - yᶦ)²

Pour la classification (log-loss) :
J(w) = -(1/m) * Σ [ yᶦ * log(f(w, xᶦ)) + (1 - yᶦ) * log(1 - f(w, xᶦ)) ]

La fonction coût est dépendante du poids w. Dans un réseau de neurones, l'essentiel est donc de trouver le(s) bon(s) poids w de f(w) qui assurent l'hyperplan de mieux distinguer les classes.

Comment trouver la combinaison w qui minimise la fonction coût ? C'est le rôle de la descente gradient.

Descente gradient
La formule célèbre de la descente gradient dépend de l’epsilon (ou taux d’apprentissage), noté alpha (α) :
w := w - α * ∇J(w)
On répète donc cette solution jusqu'à la convergence.

Dans la pratique, on combine le grand pas et le petit pas pour respectivement sauter et gagner en précision après pour que la solution converge vers le minimum de la fonction coût. Cette solution seule n'est pas suffisante, il faut aussi adopter l'une des solutions comme fixer le nombre d'itérations, tolérance sur la perte, ou encore utiliser des techniques comme le learning rate adaptatif, le momentum, ou l’early stopping.
# Requirements 
Ce projet nécessite le fichier tp_perceptron_source.py, disponible ici :
https://github.com/MitaDataAI/Perceptron/blob/master/tp_perceptron_source.py
