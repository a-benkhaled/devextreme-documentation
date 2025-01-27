When a user selects a series point, the Chart fires the [pointSelectionChanged](/api-reference/10%20UI%20Components/BaseChart/4%20Events/pointSelectionChanged.md '/Documentation/ApiReference/UI_Components/dxChart/Events/#pointSelectionChanged') event that you can handle with a function. If the handling function is not going to be changed during the lifetime of the UI component, assign it to the [onPointSelectionChanged](/api-reference/10%20UI%20Components/BaseChart/1%20Configuration/onPointSelectionChanged.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/#onPointSelectionChanged') property when you configure the UI component. To check whether a point was selected or the selection was cleared, call the [isSelected()](/api-reference/10%20UI%20Components/BaseChart/7%20Chart%20Elements/Point/3%20Methods/isSelected().md '/Documentation/ApiReference/UI_Components/dxChart/Chart_Elements/Point/Methods/#isSelected') method of the point.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#chartContainer").dxChart({
            // ...
            onPointSelectionChanged: function (e) {
                var point = e.target;
                if (point.isSelected()) {
                    // Commands to execute when the point is selected
                } else {
                    // Commands to execute when the selection is cleared
                }
            }
        });
    });

##### Angular

    <!--HTML-->
    <dx-chart
        (onPointSelectionChanged)="onPointSelectionChanged($event)">
    </dx-chart>

    <!--JavaScript-->
    import { DxChartModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        onPointSelectionChanged (e) {
            const point = e.target;
            if (point.isSelected()) {
                // Commands to execute when the point is selected
            } else {
                // Commands to execute when the selection is cleared
            }
        };
    }
    @NgModule({
        imports: [
            // ...
            DxChartModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxChart
            @point-selection-changed="onPointSelectionChanged($event)"
            ...
        >
        </DxChart>
    </template>

    <script>
    import DxChart from 'devextreme-vue/chart';

    export default {
        components: {
            DxChart
        },
        methods: {
            onPointSelectionChanged (e) {
                const point = e.target;
                if (point.isSelected()) {
                    // Commands to execute when the point is selected
                } else {
                    // Commands to execute when the selection is cleared
                }
            }
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Chart from 'devextreme-react/chart';

    class App extends React.Component {
        render() {
            return (
                <Chart
                    onPointSelectionChanged={this.onPointSelectionChanged}
                    ...
                >
                </Chart>
            );
        }

        onPointSelectionChanged (e) {
            const point = e.target;
            if (point.isSelected()) {
                // Commands to execute when the point is selected
            } else {
                // Commands to execute when the selection is cleared
            }
        }
    }

    export default App;

---

---
##### jQuery

If you are going to change the event handler at runtime, or if you need to attach several handlers to the **pointSelectionChanged** event, subscribe to this event using the [on(eventName, eventHandler)](/api-reference/10%20UI%20Components/Component/3%20Methods/on(eventName_eventHandler).md '/Documentation/ApiReference/UI_Components/dxChart/Methods/#oneventName_eventHandler') method.

    <!--JavaScript-->
    var pointSelectionChangedHandler1 = function (e) {
        var point = e.target;
        // First handler of the "pointSelectionChanged" event
    };

    var pointSelectionChangedHandler2 = function (e) {
        var point = e.target;
        // Second handler of the "pointSelectionChanged" event
    };

    $("#chartContainer").dxChart("instance")
        .on("pointSelectionChanged", pointSelectionChangedHandler1)
        .on("pointSelectionChanged", pointSelectionChangedHandler2);
        
---

#####See Also#####
#include common-link-handleevents
- [Series Selection Events](/concepts/05%20UI%20Components/Chart/10%20Series/20%20Selection/10%20Events.md '/Documentation/Guide/UI_Components/Chart/Series/Selection/#Events')
- [Chart API Reference](/api-reference/10%20UI%20Components/dxChart '/Documentation/ApiReference/UI_Components/dxChart/')
