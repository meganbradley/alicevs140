---
title: "How to: Read Application Settings in Visual Basic"
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
ms.assetid: eb3428ef-115e-49a8-a878-e0613183fee0
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Read Application Settings in Visual Basic
You can read a user setting by accessing the setting's property on the `My.Settings` object.  
  
 The `My.Settings` object exposes each setting as a property. The property name is the same as the setting name, and the property type is the same as the setting type. The setting's **Scope** indicates if the property is read-only; the property for an **Application** scope setting is read-only, while the property for a **User** scope setting is read-write. For more information, see [My.Settings Object](../Topic/My.Settings%20Object.md).  
  
## Example  
 This example displays the value of the `Nickname` setting.  
  
 [!CODE [VbVbalrMyResources#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyResources#14)]  
  
 For this example to work, your application must have a `Nickname` setting, of type `String`. For more information, see [Managing Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md).  
  
## See Also  
 [My.Settings Object](../Topic/My.Settings%20Object.md)   
 [How to: Change User Settings in Visual Basic](../vs140/How-to--Change-User-Settings-in-Visual-Basic.md)   
 [How to: Persist User Settings in Visual Basic](../vs140/How-to--Persist-User-Settings-in-Visual-Basic.md)   
 [How to: Create Property Grids for User Settings in Visual Basic](../vs140/How-to--Create-Property-Grids-for-User-Settings-in-Visual-Basic.md)   
 [Managing Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md)