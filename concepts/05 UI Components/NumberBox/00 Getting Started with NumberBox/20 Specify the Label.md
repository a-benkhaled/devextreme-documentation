You can add a label to the NumberBox and define its appearance. To display the label, assign the text to the [label](/Documentation/ApiReference/UI_Components/dxNumberBox/Configuration/#label) property. To change the label's appearance, set the [labelMode](/Documentation/ApiReference/UI_Components/dxNumberBox/Configuration/#labelMode) property to one of the following values:

- *"static"* (default)    
The component displays the label above the input field.

- *"floating"*    
The component uses the label as a placeholder, but the label moves to the position above the input field when the editor receives focus.

- *"hidden"*    
The label is hidden.


---
##### jQuery

    <!-- tab: index.js -->
    $(function() {
        $("#number-box").dxNumberBox({
            // ...
            label: "Enter a sum in dollars",
            labelMode: "floating",
        });
    });

##### Angular

    <!-- tab: app.component.html -->
    <dx-color-box ...
        label="Enter a sum in dollars"
        labelMode="floating"
    >
    </dx-color-box>

##### Vue

    <!-- tab: App.vue -->
    <template>
        <DxNumberBox ...
            label="Enter a sum in dollars"
            label-mode="floating"
        />
    </template>

    <script>
    // ...
    </script>

##### React

    <!-- tab: App.js -->
    // ...
    
    function App() {
        // ...
        return (
            <NumberBox ...
                label="Enter a sum in dollars"
                labelMode="floating"
            />
        );
    }

    export default App;

---