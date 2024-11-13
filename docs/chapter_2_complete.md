
# Chapitre 2 : Contrôle du Robot et Trigonométrie

## 1. Trigonométrie
Les robots se déplacent selon un angle et une distance. L'angle peut être calculé avec les fonctions mathématiques en Python.

## 2. Calcul de l'angle et des déplacements
En Python, vous pouvez utiliser `math.radians()` pour convertir des degrés en radians et `math.sin()` ou `math.cos()` pour calculer les coordonnées.

## 3. Exécuter un déplacement angulaire
Exemple de rotation d’un angle donné :
```python
import math

angle = 90  # Angle en degrés
angle_radian = math.radians(angle)  # Convertir en radians
print("Angle en radians :", angle_radian)
```

# Exercices du Chapitre 2

## Exercice pour Débutants
1. Complétez le code pour que le robot pivote de l’angle donné.
   ```python
   import math
   angle = ___  # Remplacez par l'angle voulu
   angle_radian = math.radians(angle)
   print("Angle en radians :", angle_radian)
   ```

## Exercice pour Avancés
2. Développez un comportement défensif où le robot se place entre la balle et le but.
   - **Objectif** : Utiliser la position de la balle pour calculer un angle et déplacer le robot en conséquence.
   - **Instructions** : Écrire le code pour calculer l’angle de rotation nécessaire et déplacez le robot en direction de la balle.
   ```python
   # Exemple de code pour une position de défenseur
   balle_x, balle_y = 50, 30
   robot_x, robot_y = 10, 10
   # Calcul de l'angle entre le robot et la balle
   angle = math.atan2(balle_y - robot_y, balle_x - robot_x)
   print("Angle de déplacement :", math.degrees(angle))
   ```
