The Map is an interactive UI component that displays a geographic map with markers and routes.

#include btn-open-demo with {
    href: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Map/ProvidersAndTypes/"
}

The code below adds the Map UI component to your page. The Map is [centered](/api-reference/10%20UI%20Components/dxMap/1%20Configuration/center '/Documentation/ApiReference/UI_Components/dxMap/Configuration/center/') and [zoomed](/api-reference/10%20UI%20Components/dxMap/1%20Configuration/zoom.md '/Documentation/ApiReference/UI_Components/dxMap/Configuration/#zoom') and supplied with [controls](/api-reference/10%20UI%20Components/dxMap/1%20Configuration/controls.md '/Documentation/ApiReference/UI_Components/dxMap/Configuration/#controls') that allow a user to [zoom and navigate](/concepts/05%20UI%20Components/Map/05%20Zoom%20and%20Center%20the%20Map.md '/Documentation/Guide/UI_Components/Map/Zoom_and_Center_the_Map/') the Map or [change its type](/concepts/05%20UI%20Components/Map/10%20Specify%20the%20Provider%20and%20Type.md '/Documentation/Guide/UI_Components/Map/Specify_the_Provider_and_Type/').

---
##### jQuery

    <!--HTML-->
    <div id="mapContainer"></div>
 
    <!--JavaScript-->
    $(function() {
        $("#mapContainer").dxMap({
            center: { lat: 40.749825, lng: -73.987963 },
            zoom: 10,
            controls: true
        });
    });

##### Angular

    <!--HTML-->
    <dx-map
        [center]="{ lat: 40.749825, lng: -73.987963 }"
        [controls]="true"
        [zoom]="10">
    </dx-map>

    <!--TypeScript-->
    import { DxMapModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxMapModule
        ],
        // ...
    })

##### Vue

    <template>
        <DxMap
            :zoom="10"
            :controls="true"
            :center="centerCoordinates"
        />
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import { DxMap } from 'devextreme-vue/map';

    export default {
        components: {
            DxMap
        },
        data() {
            return {
                centerCoordinates: { lat: 40.749825, lng: -73.987963 }
            };
        }
    }
    </script>

##### React

    import React from 'react';
    import 'devextreme/dist/css/dx.light.css';

    import { Map } from 'devextreme-react/map';

    const centerCoordinates = { lat: 40.749825, lng: -73.987963 };

    class App extends React.Component {
        render() {
            return (
                <Map
                    defaultZoom={10}
                    controls={true}
                    defaultCenter={centerCoordinates}
                />
            );
        }
    }

    export default App;

---

#####See Also#####
#include common-link-configurewidget
- [Map - Zoom and Center the Map](/concepts/05%20UI%20Components/Map/05%20Zoom%20and%20Center%20the%20Map.md '/Documentation/Guide/UI_Components/Map/Zoom_and_Center_the_Map/')
- [Map - Specify the Provider and Type](/concepts/05%20UI%20Components/Map/10%20Specify%20the%20Provider%20and%20Type.md '/Documentation/Guide/UI_Components/Map/Specify_the_Provider_and_Type/')
- [Map - Specify the Size](/concepts/05%20UI%20Components/Map/15%20Specify%20the%20Size.md '/Documentation/Guide/UI_Components/Map/Specify_the_Size/')
- [Map - Configure Markers](/concepts/05%20UI%20Components/Map/20%20Configure%20Markers/05%20Add%20and%20Remove.md '/Documentation/Guide/UI_Components/Map/Configure_Markers/')
- [Map - Configure Routes](/concepts/05%20UI%20Components/Map/25%20Configure%20Routes/05%20Add%20and%20Remove.md '/Documentation/Guide/UI_Components/Map/Configure_Routes/')
- [Map API Reference](/api-reference/10%20UI%20Components/dxMap '/Documentation/ApiReference/UI_Components/dxMap/')

[tags]dxmap, map, center, central position, zoom level, controls
