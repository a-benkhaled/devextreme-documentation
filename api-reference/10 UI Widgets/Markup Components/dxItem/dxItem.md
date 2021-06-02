---
type: Object
---
---
##### shortDescription
Specifies markup for a widget item.

---
The **dxItem** component defines custom markup for items in layout and collection widgets. **dxItem** has different options depending on the widget where it is used. See the **Default Item Template** section in a specific widget's API Reference for a full list of them.

---
#####jQuery  

    <!--HTML-->
    <div id="list">
        <div data-options="dxItem: { text: 'Apples', disabled: true }"></div>
        <div data-options="dxItem: { text: 'Lemons', visible: false }"></div>
        <div data-options="dxItem: { }">
            <!-- custom markup -->
        </div>
    </div>

    <!--JavaScript-->
    $(function() {
        $("#list").dxList({/* ... */});
    });

#####Angular

    <!-- tab: app.component.html -->
    <dx-list>
        <dxi-item text="Apples" [disabled]="true"></dxi-item>
        <dxi-item text="Lemons" [visible]="false"></dxi-item>
        <dxi-item>
            <!-- custom markup -->
        </dxi-item>
    </dx-list>

    <!-- tab: app.module.ts -->
    import { DxListModule } from "devextreme-angular";
    // ...
    @NgModule({
        imports: [
            // ...
            DxListModule
        ],
        // ...
    })
    export class AppModule { }

#####AngularJS

    <!--HTML-->
    <div dx-list="{ }">
        <div data-options="dxItem: { text: 'Apples', disabled: true }"></div>
        <div data-options="dxItem: { text: 'Lemons', visible: false }"></div>
        <div data-options="dxItem: { }">
            <!-- custom markup -->
        </div>
    </div>

    <!--JavaScript-->
    angular.module('DemoApp', ['dx'])
        .controller('DemoController', function ($scope) {
            // ...
        });

#####Knockout

    <!--HTML-->
    <div data-bind="dxList: { ... }">
        <div data-options="dxItem: { text: 'Apples', disabled: true }"></div>
        <div data-options="dxItem: { text: 'Lemons', visible: false }"></div>
        <div data-options="dxItem: { }">
            <!-- custom markup -->
        </div>
    </div>

    <!--JavaScript-->
    var viewModel = {
        // ...
    };

    ko.applyBindings(viewModel);

#####React

    <!-- tab: DxComponent.js -->
    import React from 'react';
    import List, { Item } from 'devextreme-react/list';

    class DxComponent extends React.Component {
        render() {
            return (
                <List>
                    <Item text="Apples" disabled={true} />
                    <Item text="Oranges" visible={false} />
                    <Item>
                        <!-- custom markup -->
                    </Item>
                </List>
            );
        }
    }
    export default DxComponent;

---

[note]**dxItem** elements are ignored when the **dataSource** option is defined.