---
id: dxScheduler.Options.views.appointmentTemplate
type: template
default: 'item'
---
---
##### shortDescription
Specifies a custom template for appointments.

##### param(model): Object
The data of the appointment being customized.

##### field(model.appointmentData): Object
The appointment's data object.

##### field(model.targetedAppointmentData): Object
<!-- %field(model.targetedAppointmentData)% -->

##### param(itemIndex): Number
The appointment's index.

##### param(contentElement): DxElement
#include common-ref-elementparam with { element: "appointment" }

##### return: String | UserDefinedElement
A template name or container.

---
#include btn-open-demo with {
    href: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Scheduler/CustomTemplates/"
}

#####See Also#####
- [Customize Individual Views](/concepts/05%20UI%20Components/Scheduler/060%20Views/020%20Customize%20Individual%20Views.md '/Documentation/Guide/UI_Components/Scheduler/Views/Customize_Individual_Views/')
- [Customize Appointment](/concepts/05%20UI%20Components/Scheduler/030%20Appointments/050%20Customize%20Appointment.md '/Documentation/Guide/UI_Components/Scheduler/Appointments/Customize_Appointment/')
- [Custom Templates](/concepts/05%20UI%20Components/zz%20Common/30%20Templates/10%20Custom%20Templates.md '/Documentation/Guide/UI_Components/Common/Templates/#Custom_Templates')

<!-- import * from 'api-reference\10 UI Components\dxScheduler\1 Configuration\appointmentTemplate.md' -->