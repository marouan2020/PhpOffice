🚀 Nouveau patch pour PhpOffice !

Je viens de créer un patch pour PhpOffice qui apporte deux améliorations importantes :

✅ Support des listes – Vos contenus avec listes <ul> et <ol> sont maintenant mieux rendus.
✅ Redimensionnement automatique des images – Les images respectent désormais les dimensions définies dans Word.

Ce patch facilite la conversion Word → HTML tout en conservant la mise en forme et les proportions des images.

Si vous utilisez PhpOffice dans vos projets, ce patch peut vous faire gagner beaucoup de temps et améliorer la qualité de vos exports !


# PhpOffice
Support des listes et redimensionnement des images dans PhpOffice.

### Composer
```sh
composer require phpoffice/phpword
```
## Installation
Ajouter le patch dans composer.json
```sh
"extra": {
    "patches": {
        "phpoffice/phpword": {
            "Fix phpword reader writer": "[PATHTOYOURPATCH]/phpofficeWord.patch"
        }
    }
}
```

Modifications principales :
- Ajout du support des objets ListItemRun dans la génération de contenu.
- Détection du type de liste "(ordonnée ol ou non ordonnée ul)".
- Encapsulation automatique des éléments de liste avec ul/ol et li.
- Amélioration de la gestion des blocs de texte pour éviter les pertes de formatage.
- Redimensionnement des images en respectant les dimensions définies dans le document Word.

Ces changements permettent d'obtenir une conversion plus fidèle des documents Word, avec une meilleure prise en charge des listes et un rendu des images cohérent avec la mise en page originale.

Contact: marouan.ben.mansour@gmail.com
