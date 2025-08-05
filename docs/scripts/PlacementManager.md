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
            /*fait qlq chose*/
        }
    }

    private bool IsValidPosition(Vector3 pos)
    {
        return true;
    }
}
```

### Méthode : SelectObject(GameObject obj)
- Change la couleur de l’objet pour indiquer qu’il est sélectionné.
- Stocke une référence à l’objet sélectionné.
OU 
- `SelectObject(GameObject obj)` : sélectionne un objet et change sa couleur.  

### Méthode : DragObject        
- `DragObject(GameObject obj, Vector3 newPos)` : déplace un objet sélectionné si la position est valide.

## Variables 

- `selectedObject` : objet actuellement sélectionné.  
- `dragSpeed` : vitesse de déplacement lors du drag.

## Interactions

Interacte avec les scripts :  
- TODO (doit etre un hyperlink vers le script concerné ?)
- TODO 

## TODO
- Implémenter IsValidPosition() 
- ect...