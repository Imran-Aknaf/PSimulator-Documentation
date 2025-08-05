# Script : PlacementManager

## Description

TODO
 
## Classes et méthodes

### Classe : PlacementManager

```csharp
public class PlacementManager : MonoBehaviour
{
    public GameObject selectedObject;
    public float dragSpeed = 5f;

    public void SelectObject(GameObject obj)
    {
        selectedObject = obj;
        obj.GetComponent<Renderer>().material.color = Color.green;
    }

    public void DragObject(Vector3 newPos)
    {
        if (IsValidPosition(newPos))
        {
            selectedObject.transform.position = Vector3.Lerp(
                selectedObject.transform.position,
                newPos,
                Time.deltaTime * dragSpeed
            );
        }
    }

    private bool IsValidPosition(Vector3 pos)
    {
        // TODO: vérifier collisions, limites, points autorisés
        return true;
    }
}
```

### Méthode : SelectObject(GameObject obj)
- Change la couleur de l’objet pour indiquer qu’il est sélectionné.
- Stocke une référence à l’objet sélectionné.

- `SelectObject(GameObject obj)` : sélectionne un objet et change sa couleur.  

### Méthode : DragObject        
- `DragObject(GameObject obj, Vector3 newPos)` : déplace un objet sélectionné si la position est valide.

## Variables importantes

- `selectedObject` : objet actuellement sélectionné.  
- `dragSpeed` : vitesse de déplacement lors du drag.

## Interactions

Interacte avec les scripts :  
- [SpawnerController](SpawnerController.md) pour le spawn dynamique.  
- [UIManager](UIManager.md) pour les retours visuels.

## TODO
- Implémenter IsValidPosition() selon la logique métier
- Ajouter un feedback visuel en cas de position invalide
- Intégrer avec le système de sauvegarde