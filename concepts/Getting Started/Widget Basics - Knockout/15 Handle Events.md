You can subscribe to an event using a configuration property. All event handling properties are given names that begin with *on*.

    <!--JavaScript-->
    var viewModel = {
        menuInstance: {},
        menuOptions: {
            // ...
            onItemClick: function (info) {
                // Handles the "itemClick" event
            },
            onInitialized: function (info) {
                // Saves the UI component instance
                viewModel.menuInstance = info.component;    
                // Handles the "initialized" event
            }
        }
    };

    ko.applyBindings(viewModel);

#include btn-open-demo with {
    href: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Menu/Overview/Knockout/Light/"
}

#####See Also#####
- **API Reference**.**WidgetName**.**Events**, for example, **API Reference**.[Menu](/api-reference/10%20UI%20Components/dxMenu '/Documentation/ApiReference/UI_Components/dxMenu/').[Events](/api-reference/10%20UI%20Components/dxMenu/4%20Events '/Documentation/ApiReference/UI_Components/dxMenu/Events/')

[tags]basics, knockout, handle events, subscribe