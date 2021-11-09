---
uid: gpTypes
---

# Add a type

Sequential Data Store (SDS) types define the shape and structure of events and how to associate events with streams of data. After you have created a type, it cannot be modified.

To add a type, follow these steps:

1. In the left pane, select **Data Management** > **Sequential Data Store**.

1. From the **Streams** dropdown list, select **Types** if it is not already selected.

1. Click **Add Type**.

1. In the `Add Type` pane, complete the following fields:

   - **Id** &ndash; Enter an Id for referencing the type.
    
   - **Name** &ndash; (Optional) Enter a user-friendly name. If you do not provide a name, the Id will be assigned as the name.
   
   - **Description** &ndash; (Optional) Enter descriptive text to identify the type.
   
   - **Base Type** &ndash; (Optional) To base the new type on an existing type, select the existing type from the dropdown. The new type inherits the properties of the base type. Inherited properties are read only and cannot be modified.

1. For each property to add to the type, select **Add Property** and complete the following:
 
   - **Key** &ndash;  Select the checkbox to identify the property as the index. Only system SDS types can be designated as keys. 

     **Note:** You can select up to three properties as indexes. Drag and drop the properties in the list to reorder the index keys.
   
   - **Id** &ndash; Enter an identifier for referencing the property.
   
   - **Name** &ndash; Enter a name for the property. By default, the `Id` and `Name` are the same. 
   
   - **Type** &ndash; Select the SDS type of the property from the dropdown.
   
     **Note:** To find the type in the list, filter on the property types by entering text in the **Filter Types** box and use the **System** or **Tenant** controls to include or exclude these types. *Tenant* includes any types that were previously created in the selected namespace for a particular tenant. *System* includes SDS types that are provided and defined such as *string*, *integer*, *double*, *datetime*, and *boolean*.
   
   - **UOM** &ndash; (Optional) Select a unit of measure for the property from the list. 

1. To save the type, select **Save**.
