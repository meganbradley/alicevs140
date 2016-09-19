---
title: "How to: Change User Settings in Visual Basic"
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
ms.assetid: 41250181-c594-4854-9988-8183b9eb03cf
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Change User Settings in Visual Basic
You can change a user setting by assigning a new value to the setting's property on the `My.Settings` object.  
  
 The `My.Settings` object exposes each setting as a property. The property name is the same as the setting name, and the property type is the same as the setting type. The setting's **Scope** determines if the property is read-only: The property for an **Application**-scope setting is read-only, while the property for a **User**-scope setting is read-write. For more information, see [My.Settings Object](../Topic/My.Settings%20Object.md).  
  
> [!NOTE]
>  Although you can change and save the values of user-scope settings at run time, application-scope settings are read-only and cannot be changed programmatically. You can change application-scope settings when you create the application by using the **Project Designer** or by editing the application's configuration file. For more information, see [Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md).  
  
## Example  
 This example changes the value of the `Nickname` user setting.  
  
 [!CODE [VbVbalrMyResources#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyResources#7)]  
  
 For this example to work, your application must have a `Nickname` user setting, of type `String`.  
  
 The application saves the user settings when the application shuts down. To save the settings immediately, call the `My.Settings.Save` method. For more information, see [How to: Persist User Settings in Visual Basic](../vs140/How-to--Persist-User-Settings-in-Visual-Basic.md).  
  
## See Also  
 [My.Settings Object](../Topic/My.Settings%20Object.md)   
 [How to: Read Application Settings in Visual Basic](../vs140/How-to--Read-Application-Settings-in-Visual-Basic.md)   
 [How to: Persist User Settings in Visual Basic](../vs140/How-to--Persist-User-Settings-in-Visual-Basic.md)   
 [How to: Create Property Grids for User Settings in Visual Basic](../vs140/How-to--Create-Property-Grids-for-User-Settings-in-Visual-Basic.md)   
 [Managing Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md)