---
title: "Customizing Entity Fields in LightSwitch"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - lightswitch
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76df3105-23b6-4a1c-9d0d-648e2e3a7a29
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Customizing Entity Fields in LightSwitch
In this lesson, you’ll learn how to set properties and change the data type for fields in a data entity in LightSwitch.  
  
## Customize Entity Fields  
 By setting the `Summary Property` for an entity, you specify the field that is used to describe the entity type when used on screens. For example, the default `Summary Property` for the **Contacts** entity is the **Id** field. In this case it’s better to set the `Summary Property` to a field with a more meaningful name. such as **CompanyName**.  
  
#### To set the summary property  
  
1.  In **Solution Explorer**, open the shortcut menu for the **Customers.lsml** node, and then choose **Open**.  
  
     The **Data Designer** opens.  
  
2.  On the **Perspective** bar, choose the **HTMLClient** tab.  
  
3.  In the **Properties** window, in the **Summary Property** list, choose **CompanyName**.  
  
 By setting display properties, you specify how the data for a given field appears to the user. For example, for a field named CompanyName you might want to display it to the user as simply “Company”.  
  
#### To change a display name  
  
1.  In the **Data Designer**, choose the **CompanyName** field.  
  
2.  In the **Properties** window, choose the **Display Name** property, and then enter **Company** in the text box.  
  
 By setting the `Description` property for a field you can provide text that is displayed to the user as a tooltip in the running application.  
  
#### To set the description property  
  
1.  In the **Data Designer**, choose the **ContactName** field.  
  
2.  In the **Properties** window, choose the **ContactName** property text box and enter **This is our primary contact at this company**.  
  
     The value of the **Description** property appears as a tooltip in the application when a user points to a field.  
  
 Fields in a database table are often stored in a format that's efficient for the database but may not be what you want to display to the user. For example, fields that represent monetary values are typically stored as a `Decimal` data type,. For display purposes, you would usually want to format the values with a currency symbol and the correct number of decimal places.  
  
#### To change data types  
  
1.  In **Solution Explorer**, open the shortcut menu for the **Customers** node, and then choose **Open**.  
  
2.  In the **Data Designer**, on the **Perspective** bar, choose the **Server** tab.  
  
3.  In the **Properties** window, choose the **ContactName** property text box and enter **This is our primary contact at this company**.  
  
     The value of the **Description** property appears as a tooltip in the application when a user points to a field.  
  
4.  In the **Type** column, open the list, and then choose **PhoneNumber**.  
  
     **PhoneNumber** is a custom business type that displays a telephone number in a standardized format. You can specify the valid formats for your application by choosing the **Phone Number Formats** property.  
  
5.  In **Solution Explorer**, open the shortcut menu for the **Order_Details** node, and then choose **Open**.  
  
6.  In the **Data Designer**, on the **Perspective** bar, choose the **Server** tab.  
  
7.  Choose the **UnitPrice** field.  
  
8.  In the **Type** column, open the list, and then choose **Money**.  
  
     **Money** is another custom business type for formatting and displaying currency values.  
  
9. In the **Properties** window, choose the **Currency Symbol** property and enter `$` in the text box.  
  
10. Choose the **Decimal Places** property and enter `2` in the text box.  
  
## Closer Look  
 In this lesson, you set properties for entity fields and you changed the data type of a field. It's good practice to customize display properties and data types immediately after you add an entity, but you can do this at any time during application development.  
  
 The first property that you set was the **Summary** property. For screens that contain lists, this field appears in the list instead of the default ID field.  
  
 Database field names can’t contain spaces, and sometimes use an underscore character to represent a space. To ensure that the field names displayed to your users are clear and easy to understand, you can revise the field names and add spaces in LightSwitch. To do this, review the field names in your database entities, and change the **Display Name** property for any fields that require a better display name.  
  
 Most of the properties that you can set are related to appearance, but others set validation rules and other characteristics. Availability of properties varies by data type. Later lessons describe other properties.  
  
 By using a custom data type, you can present data in a way that's most appropriate for your application without changing a type in the underlying database. For example, the `Money` custom type converts the decimal format in the database to a currency format in the display, while the database retains its efficient decimal format. Many custom data types provide type-specific properties. For example, the `Currency Symbol` property for the `Money` type determines how currency is displayed to users.  
  
 In addition to the `PhoneNumber` and `Money` custom business types, LightSwitch also provides the `EmailAddress`, `Hyperlink`, `Percentage`, `Web Address`, and `Image` types.  
  
> [!NOTE]
>  Images are often stored in a database as a `Binary` data type. You can't display a `Binary` type, but you can change it to the `Image` type for display purposes.  
  
## Next Steps  
 In the next lesson, you’ll learn how to present a list of predetermined values to the user. Next lesson: [Presenting a List of Choices](../vs140/Presenting-a-List-of-Choices-in-a-LightSwitch-Application.md)  
  
## See Also  
 [Working with Data in LightSwitch](../vs140/Working-with-Data-in-LightSwitch.md)   
 [How to: Define Data Fields](../vs140/How-to--Define-Data-Fields-in-a-LightSwitch-Database.md)   
 [How to: Validate Data](../vs140/How-to--Validate-Data-in-a-LightSwitch-Application.md)   
 [Extensions: Adding New Capabilities to LightSwitch](../vs140/Extensions--Adding-New-Capabilities-to-LightSwitch.md)