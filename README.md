README.md` :

```markdown
# Analyse de Phrase - Algorithme

## Description

Cet algorithme analyse une phrase entrée par l'utilisateur. Il permet de calculer la longueur de la phrase, le nombre de mots et le nombre de voyelles qu'elle contient. La phrase saisie doit obligatoirement se terminer par un point. 

L'algorithme parcourt chaque caractère de la phrase et effectue plusieurs contrôles :

- **Longueur de la phrase** : L'algorithme compte chaque caractère de la phrase, y compris les espaces et les voyelles.
- **Nombre de mots** : L'algorithme détermine le nombre de mots en comptant les espaces qui séparent les mots. Il tient également compte du point final.
- **Nombre de voyelles** : Il compte le nombre de voyelles dans la phrase en se basant sur les lettres définies dans la chaîne `"aeiouyAEIOUY"`.

## Fonctionnement de l'algorithme

1. **Initialisation** : L'algorithme commence par initialiser trois variables :
   - `longueur` : qui compte la longueur totale de la phrase.
   - `nombre_mots` : qui compte le nombre de mots dans la phrase.
   - `nombre_voyelles` : qui compte le nombre de voyelles.
   - La chaîne de caractères `voyelles` contient toutes les voyelles majuscules et minuscules.

2. **Lecture de la phrase** : L'algorithme demande à l'utilisateur de saisir une phrase. Cette phrase doit se terminer par un point.

3. **Traitement caractère par caractère** :
   - **Si un caractère est une voyelle** : Le compteur `nombre_voyelles` est incrémenté.
   - **Si un caractère est un espace** : Cela marque la fin d'un mot et permet de commencer un nouveau mot.
   - **Si un caractère est un point** : L'algorithme termine la lecture et effectue le dernier comptage des mots, puis sort de la boucle.

4. **Affichage des résultats** : Une fois la phrase analysée, l'algorithme affiche :
   - La longueur totale de la phrase.
   - Le nombre de mots.
   - Le nombre de voyelles.

## Pseudocode

```text
Début
    Initialiser longueur à 0
    Initialiser nombre_mots à 0
    Initialiser nombre_voyelles à 0
    Définir la chaîne voyelles = "aeiouyAEIOUY"
    Initialiser mot_en_cours à Faux

    Afficher "Entrez une phrase qui se termine par un point :"
    
    Tant que vrai
        Lire un caractère
        Si le caractère n'est pas un seul caractère
            Afficher "Veuillez entrer un seul caractère à la fois"
            Continuer la boucle

        Ajouter 1 à longueur
        
        Si le caractère est une voyelle (présente dans voyelles)
            Ajouter 1 à nombre_voyelles

        Si le caractère est un espace
            Mettre mot_en_cours à Faux

        Sinon, si le caractère est un point "."
            Si mot_en_cours est vrai
                Ajouter 1 à nombre_mots
            Fin de la boucle

        Sinon
            Si mot_en_cours est faux
                Ajouter 1 à nombre_mots
            Mettre mot_en_cours à vrai

    Afficher "Résultats :"
    Afficher "Longueur de la phrase : " + longueur
    Afficher "Nombre de mots : " + nombre_mots
    Afficher "Nombre de voyelles : " + nombre_voyelles
Fin
```

## Explication du Pseudocode

1. **Initialisation** : Avant de commencer à lire la phrase, l'algorithme initialise les compteurs à zéro.
2. **Lecture des caractères** : L'algorithme lit chaque caractère de la phrase et fait des vérifications sur chaque caractère (s'il est une voyelle, un espace ou un point).
3. **Comptage des voyelles** : Si le caractère est une voyelle, le compteur `nombre_voyelles` est incrémenté.
4. **Comptage des mots** : L'algorithme reconnaît un mot lorsqu'il rencontre un espace ou à la fin de la phrase.
5. **Affichage des résultats** : Après la lecture de la phrase, l'algorithme affiche la longueur totale, le nombre de mots et le nombre de voyelles.



