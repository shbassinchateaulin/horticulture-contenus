# Publisher automatique

L’administrateur ne crée jamais de dossier GitHub manuellement.

Le service reçoit une publication structurée et `publish.mjs` :

1. attribue automatiquement `A0000001…` (actualité) ou `S0000001…` (sortie) ;
2. crée le dossier autonome correspondant et `medias/` ;
3. écrit `contenu.json`, `layout.json` et `media.json` ;
4. compte photos, documents et phrases ;
5. active automatiquement la galerie au-delà de 9 photos ;
6. accepte un nombre variable de documents ;
7. reconstruit l’index de la collection ;
8. ne classe jamais une actualité en événement futur simplement parce que son texte mentionne une prochaine réunion : il faut un champ `event.startDate` structuré.

## Images

La conversion WebP doit avoir lieu à l’entrée du service d’upload, avant l’appel au publisher. Le navigateur public ne convertit rien. Les chemins WebP produits sont ensuite transmis dans `photos`.

## Contrat minimal

```json
{
  "type": "actualite",
  "title": "Titre",
  "text": "Texte",
  "layoutCode": "H15",
  "photos": [],
  "documents": []
}
```

Les identifiants, dossiers, compteurs, galerie et index sont automatiques.