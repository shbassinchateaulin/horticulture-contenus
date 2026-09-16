# Horticulture — contenus

Stockage structuré des actualités de la Société d’Horticulture et d’Art Floral du Bassin de Châteaulin.

Ce dépôt contient les index, manifestes et compositions. Les consommateurs (site public et application d’administration) ne doivent jamais dépendre directement de l’emplacement physique d’un média : ils utilisent les identifiants permanents des actualités et les manifestes.

## Principes

- identifiants permanents `actu-0001`, `actu-0002`, … ;
- aucune renumérotation après suppression ;
- une actualité n’est jamais fragmentée entre plusieurs lots de médias ;
- l’emplacement des médias est une donnée technique invisible pour l’interface d’administration ;
- la composition d’une actualité est calculée une fois puis enregistrée ;
- le responsive reste géré par le moteur du site ;
- le stockage des médias peut être remplacé ultérieurement sans modifier le contrat de données public.

Voir `schema/architecture.json` pour le contrat de stockage et `actualites/index.json` pour l’index public.
