---
title: "Rapid Application Development with My.Resources and My.Settings (Visual Basic)"
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
ms.assetid: 68284ab1-b685-4814-a2a4-01ae40445ff8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Rapid Application Development with My.Resources and My.Settings (Visual Basic)
The `My.Resources` object provides access to the application's resources and allows you to dynamically retrieve resources for your application.  
  
## Retrieving Resources  
 A number of resources such as audio files, icons, images, and strings can be retrieved through the `My.Resources` object. For example, you can access the application's culture-specific resource files. The following example sets the icon of the form to the icon named `Form1Icon` stored in the application's resource file.  
  
 [!CODE [VbVbcnMy#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMy#7)]  
  
 The `My.Resources` object exposes only global resources. It does not provide access to resource files associated with forms. You must access the form resources from the form. For more information, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5).  
  
 Similarly, the `My.Settings` object provides access to the application's settings and allows you to dynamically store and retrieve property settings and other information for your application. For more information, see [My.Resources Object](../Topic/My.Resources%20Object.md) and [My.Settings Object](../Topic/My.Settings%20Object.md).  
  
## See Also  
 [My.Resources Object](../Topic/My.Resources%20Object.md)   
 [My.Settings Object](../Topic/My.Settings%20Object.md)   
 [Accessing Application Settings](../vs140/Accessing-Application-Settings--Visual-Basic-.md)