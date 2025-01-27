---
id: dxDiagram.getItemByKey(key)
---
---
##### shortDescription
Returns a [shape](/api-reference/50%20Common/Object%20Structures/dxDiagramShape '/Documentation/ApiReference/Common/Object_Structures/dxDiagramShape/') or [connector](/api-reference/50%20Common/Object%20Structures/dxDiagramConnector '/Documentation/ApiReference/Common/Object_Structures/dxDiagramConnector/') object specified by its key.

##### return: dxDiagramItem
A **dxDiagramItem** object descendant (dxDiagramShape or dxDiagramConnector).

##### param(key): Object
The item key.

---
An item key specifies the item's identifier in a data source. If a diagram is not bound to a data source, the key value is empty. In this instance, use the [GetItemById(id)](/api-reference/10%20UI%20Components/dxDiagram/3%20Methods/getItemById(id).md '/Documentation/ApiReference/UI_Components/dxDiagram/Methods/#getItemByIdid') method to get an item by its internal identifier. An item always has an identifier.