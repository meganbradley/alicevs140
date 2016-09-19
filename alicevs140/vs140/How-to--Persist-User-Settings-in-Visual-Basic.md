---
title: "How to: Persist User Settings in Visual Basic"
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
ms.assetid: 0e5e6415-b6e2-4602-9be0-a65fa167d007
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Persist User Settings in Visual Basic
You can use the `My.Settings.Save` method to persist changes to the user settings.  
  
 Typically, applications are designed to persist the changes to the user settings when the application shuts down. This is because saving the settings can take, depending on several factors, several seconds.  
  
 For more information, see [My.Settings Object](../Topic/My.Settings%20Object.md).  
  
> [!NOTE]
>  Although you can change and save the values of user-scope settings at run time, application-scope settings are read-only and cannot be changed programmatically. You can change application-scope settings when creating the application, through the **Project Designer**, or by editing the application's configuration file. For more information, see [Managing Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md).  
  
## Example  
 This example changes the value of the `LastChanged` user setting and saves that change by calling the `My.Settings.Save` method.  
  
 [!CODE [VbVbalrMyResources#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyResources#5)]  
  
 For this example to work, your application must have a `LastChanged` user setting, of type `Date`. For more information, see [Managing Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md).  
  
## See Also  
 [My.Settings Object](../Topic/My.Settings%20Object.md)   
 [How to: Read Application Settings in Visual Basic](../vs140/How-to--Read-Application-Settings-in-Visual-Basic.md)   
 [How to: Change User Settings in Visual Basic](../vs140/How-to--Change-User-Settings-in-Visual-Basic.md)   
 [How to: Create Property Grids for User Settings in Visual Basic](../vs140/How-to--Create-Property-Grids-for-User-Settings-in-Visual-Basic.md)   
 [Managing Application Settings](../Topic/Managing%20Application%20Settings%20\(.NET\).md)