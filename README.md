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
## Sur la fonction de décision 
- Géométriquement, c'est l'hyperplan qui sépare les classes. Elle est idéalle si elle maximise donc la distance entre les classes. Dans la pratique, il y a un chevauchement entre les points.   
- Algébriquement, l'hyperplan le plus simple est une droite de forme f(w) = w0, w1*x1. w1 est le poids. Dans la pratique, cette forme peut avoir plusieurs variables X. 
- La fonction de décision peut avoir la forme de droite mais aussi d'autres formes géométriques : ellipse, parabole, etc. L'efficacité de la forme dépend de la distribution des données.
- Dans l'espace des données, il existe une infinité possible de fonction de décision pour une forme données. Pour trouver la fonction de décision optimale, c'est là qu'entre en jeu la fonction de cout et la descente gradiente.
- Bien qu'il y a des variantes, la fonction cout minimise en général l'écart entre la prédiction (f(W)) et la valeure réelle. Chaque observation a un cout. Au lieu de minimiser tous les couts, on minimise la fonction cout moyenne à préciser ... 
- La fonction cout est dépendante du poids W. Dans un réseau de neuronne, l'essentiel est donc de trouver le(s) bon(s) poids W de f(W) qui assurent l'hyperplan de mieux distinguer les classes.
- Comment trouver la combiner W qui minimise la fonction cout? C'est le rôle de la descente gradient.
- La formule célèbre de la descente gradiente dépend de l'espisolne ... On répète donc cette solution jusqu'à la convergence. 
- Dans la pratique, on combine le grand pas et le petit pas pour respectivement sauter et gagner en précision après pour que la solution converge vers le minimum de la fonction cout. Cette solution seule n'est pas suffisante, il faut aussi adopter l'une des solutions comme fixer le nombre d'itérations, tolérance sur la perte.    

# Requirements 
Ce projet nécessite le fichier tp_perceptron_source.py, disponible ici :
https://github.com/MitaDataAI/Perceptron/blob/master/tp_perceptron_source.py