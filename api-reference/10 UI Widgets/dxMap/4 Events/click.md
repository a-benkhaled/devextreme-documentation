---
type: eventType
---
---
##### shortDescription
Raised when any location on the map is clicked.

##### param(e): Object
Information about the event.

##### field(e.component): {WidgetName}
The widget's instance.

##### field(e.element): dxElement
The widget's container. It is an [HTML Element](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement) or a [jQuery Element](https://api.jquery.com/Types/#jQuery) when you use jQuery.

##### field(e.model): Object
The model data. Available only if Knockout is used.

##### field(e.location): Object
The clicked point's location on the map (if the "google" or "bing" provider is used).

##### field(e.jQueryEvent): jQuery.Event
The jQuery event that caused the handler execution (if a static google provider is used). Deprecated in favor of the **event** field.

##### field(e.jQueryEvent).deprecated
Use 'event' instead.

##### field(e.event): event
The event that caused the handler execution. It is a [dxEvent](/api-reference/50%20Common/Object%20Structures/dxEvent '/Documentation/ApiReference/Common/Object_Structures/dxEvent/') or a [jQuery.Event](https://api.jquery.com/category/events/event-object) when you use jQuery.

---
Main article: [onClick](/api-reference/10%20UI%20Widgets/dxMap/1%20Configuration/onClick.md '/Documentation/ApiReference/UI_Widgets/dxMap/Configuration/#onClick')

#####See Also#####
#include common-link-handleevents