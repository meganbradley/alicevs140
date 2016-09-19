---
title: "How to: Create Property Grids for User Settings in Visual Basic"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b0bc737e-50d1-43d1-a6df-268db6e6f91c
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create Property Grids for User Settings in Visual Basic
You can create a property grid for user settings by populating a <xref:System.Windows.Forms.PropertyGrid?qualifyHint=False> control with the user setting properties of the `My.Settings` object.  
  
> [!NOTE]
>  In order for this example to work, your application must have its user settings configured. For more information, see [Managing Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md).  
  
 The `My.Settings` object exposes each setting as a property. The property name is the same as the setting name, and the property type is the same as the setting type. The setting's **Scope** determines if the property is read-only; the property for an **Application**-scope setting is read-only, while the property for a **User**-scope setting is read-write. For more information, see [My.Settings Object](../Topic/My.Settings%20Object.md).  
  
> [!NOTE]
>  You cannot change or save the values of application-scope settings at run time. Application-scope settings can be changed only when creating the application (through the **Project Designer**) or by editing the application's configuration file. For more information, see [Managing Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md).  
  
 This example uses a <xref:System.Windows.Forms.PropertyGrid?qualifyHint=False> control to access the user-setting properties of the `My.Settings` object. By default, the <xref:System.Windows.Forms.PropertyGrid?qualifyHint=False> shows all the properties of the `My.Settings` object. However, the user-setting properties have the <xref:System.Configuration.UserScopedSettingAttribute?qualifyHint=False> attribute. This example sets the <xref:System.Windows.Forms.PropertyGrid.BrowsableAttributes?qualifyHint=False> property of the <xref:System.Windows.Forms.PropertyGrid?qualifyHint=False> to <xref:System.Configuration.UserScopedSettingAttribute?qualifyHint=False> to display only the user-setting properties.  
  
### To add a user setting property grid  
  
1.  Add the **PropertyGrid** control from the **Toolbox** to the design surface for your application, assumed here to be `Form1`.  
  
     The default name of the property-grid control is `PropertyGrid1`.  
  
2.  Double-click the design surface for `Form1` to open the code for the form-load event handler.  
  
3.  Set the `My.Settings` object as the selected object for the property grid.  
  
     [!CODE [VbVbalrMyResources#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyResources#11)]  
  
4.  Configure the property grid to show only the user settings.  
  
     [!CODE [VbVbalrMyResources#12](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyResources#12)]  
  
    > [!NOTE]
    >  To show only the application-scope settings, use the <xref:System.Configuration.ApplicationScopedSettingAttribute?qualifyHint=False> attribute instead of  <xref:System.Configuration.UserScopedSettingAttribute?qualifyHint=False>.  
  
## Robust Programming  
 The application saves the user settings when the application shuts down. To save the settings immediately, call the `My.Settings.Save` method. For more information, see [How to: Persist User Settings in Visual Basic](../vs140/How-to--Persist-User-Settings-in-Visual-Basic.md).  
  
## See Also  
 [My.Settings Object](../Topic/My.Settings%20Object.md)   
 [How to: Read Application Settings in Visual Basic](../vs140/How-to--Read-Application-Settings-in-Visual-Basic.md)   
 [How to: Change User Settings in Visual Basic](../vs140/How-to--Change-User-Settings-in-Visual-Basic.md)   
 [How to: Persist User Settings in Visual Basic](../vs140/How-to--Persist-User-Settings-in-Visual-Basic.md)   
 [Managing Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md)