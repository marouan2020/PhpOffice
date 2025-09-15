# PhpOffice
Support des listes et redimensionnement des images dans PhpOffice.

## Installation
Ajouter le patch dans composer.json
```sh
"extra": {
    "patches": {
        "phpoffice/phpword": {
            "Fix phpword reader writer": "https://github.com/marouan2020/PhpOffice/blob/main/phpofficeWord.patch"
        }
    }
}
```

### Composer
```sh
composer require phpoffice/phpword
```

Modifications principales :
- Ajout du support des objets ListItemRun dans la génération de contenu.
- Détection du type de liste "(ordonnée ol ou non ordonnée ul)".
- Encapsulation automatique des éléments de liste avec ul/ol et li.
- Amélioration de la gestion des blocs de texte pour éviter les pertes de formatage.
- Redimensionnement des images en respectant les dimensions définies dans le document Word.

Ces changements permettent d'obtenir une conversion plus fidèle des documents Word, avec une meilleure prise en charge des listes et un rendu des images cohérent avec la mise en page originale.

Contact: marouan.ben.mansour@gmail.com
