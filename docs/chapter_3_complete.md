
# Chapitre 3 : Stratégies et Comportements Avancés

## 1. Stratégies de Match
Chaque rôle (attaquant, défenseur, gardien) a des comportements spécifiques basés sur la position de la balle et des robots adverses.

## 2. Utilisation des Conditions et des Boucles
Les conditions permettent de prendre des décisions en fonction de la situation de jeu.

## 3. Exemple : Éviter une pénalité
Si un robot reste trop longtemps près de la balle, il doit s’en éloigner pour éviter les pénalités.

# Exercices du Chapitre 3

## Exercice pour Débutants
1. Créez une stratégie de base pour que le robot suive la balle sur le terrain :
   - **Objectif** : Déplacez le robot en suivant la balle avec une distance constante.
   - **Instructions** : Utilisez des conditions pour adapter la distance.
   ```python
   balle_x, balle_y = 50, 50
   robot_x, robot_y = 45, 45
   # Code pour déplacer le robot en suivant la balle
   ```

## Exercice pour Avancés
2. Implémentez une stratégie pour éviter la pénalité :
   - **Objectif** : Le robot doit s’éloigner de la balle après être resté à côté plus de 3 secondes.
   - **Instructions** : Utilisez une condition avec un chronomètre pour contrôler le comportement du robot.
   ```python
   import time

   temps_proche_balle = 0
   position_balle_x, position_balle_y = 50, 50
   position_robot_x, position_robot_y = 48, 48

   while True:
       # Vérifiez la distance entre le robot et la balle
       if abs(position_robot_x - position_balle_x) < 5 and abs(position_robot_y - position_balle_y) < 5:
           temps_proche_balle += 1  # Incrémentez si proche
           if temps_proche_balle >= 3:
               print("S'éloigner de la balle pour éviter la pénalité")
               break
       else:
           temps_proche_balle = 0  # Réinitialiser si loin
       time.sleep(1)
   ```
