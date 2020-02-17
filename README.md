# Info1-TIN-1-A - 2019/2020 - Labo01 "Tri de texte"

## **Objectifs**
Les principaux buts de ce travail de laboratoire sont :
- utiliser les chaînes de caractères et les tableaux,
- tester votre code.

## **Durée**
La durée encadrée de ce labo est de 4 x 45 minutes.

## **Qualité du code C**
-  un commentaire au début du fichier source devra mentionner le nom du labo, votre nom et prénom,
-  un commentaire à la fin du fichier source devra exposer les tests que vous avez réalisés,
-  si nécessaire, quelques commentaires pourront être placés dans le code source afin d'aider le lecteur à comprendre,
-  nommez correctement vos variables,
-  choisissez correctement les types de données,
-  respectez les noms imposés pour les fonctions,
-  lors de toute saisie de valeur numérique, vous devez prendre les précautions d'usage pour un fonctionnement correct, même si l'utilisateur saisit un donnée inadaptée.

## **Cahier des charges**

Vous devez programmer un logiciel en C permettant de trier des chaînes de caractères passées en arguments au programme. L'affichage des chaînes triées sera réalisé **exactement** comme indiqué ci-dessous.

Pour que le programme fonctionne correctement, on considère que le nombre maximum de chaînes à trier doit être compris entre `1` et `30` (valeurs incluses).

La taille maximale d'une chaîne (`\0` inclus) est de 128 caractères.

```bash
> ./app --names chien chat poule mouton cheval
chat, cheval, chien, mouton, poule.
```

```bash
> ./app --sort sed ut perspiciatis unde omnis iste natus error sit
error, iste, natus, omnis, perspiciatis, sed, sit, unde, ut.
```


```bash
> ./app --sort "un chat" "des chiens" "trois poules" "quatre pattes"                                           
des chiens, quatre pattes, trois poules, un chat.
```


```bash
> ./app --count "un chat" "des chiens" "trois poules" "quatre pattes"      
count: 4
```

```bash
> ./app
Usage for ./app:
        ./app --help : display this.
        ./app --sort [strings] : sort and display the strings.
        ./app --count [strings] : display the number of strings.
```
```bash
> ./app --help
Usage for ./app:
        ./app --help : display this.
        ./app --sort [strings] : sort and display the strings.
        ./app --count [strings] : display the number of strings.
```

<div style="page-break-after: always;"></div>

## **Prototypes des fonctions imposées**

Pour l'affichage du "comment" utiliser le programme, option `--help` :
```C
void usage(const char* appName);
```

Pour l'affichage des `numNames` noms contenus dans le tableau `names` :
```C
int printNames(uint32_t numNames, char names[][NAME_MAX_SIZE])
```

Pour le tri (selon le code ASCII) des `numNames` noms contenus dans le tableau `names` :
```C
void sortNames(const uint32_t numNames, char names[][NAME_MAX_SIZE])
```


## **Code retour du programme**

| cas | code retour |
|---|---|
| option --help | 0 |
| aucune option | 254 |
| option --sort suivie de plus que 30 chaînes | 253 |
| option --sort suivie d'aucune chaîne | 253 |
| option --sort suivie de 1 à 30 chaînes | 0 |
| option --count suivie de plus que 30 chaînes | 253 |
| option --count suivie d'aucune chaîne | 253 |
| option --count suivie de 1 à 30 chaînes | nombre de chaînes |




## **Délai**

Les travaux sont à rendre impérativement **le dimanche 22 décembre 2019 à 23h55**.
