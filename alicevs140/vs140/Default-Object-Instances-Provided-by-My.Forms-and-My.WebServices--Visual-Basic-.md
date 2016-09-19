---
title: "Default Object Instances Provided by My.Forms and My.WebServices (Visual Basic)"
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
ms.assetid: de930027-9108-4f0c-b97c-5e7db4d6ef79
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Default Object Instances Provided by My.Forms and My.WebServices (Visual Basic)
The [My.Forms](../Topic/My.Forms%20Object.md) and [My.WebServices](../Topic/My.WebServices%20Object.md) objects provide access to forms, data sources, and XML Web services used by your application. They do this by providing collections of *default instances* of each of these objects.  
  
## Default Instances  
 A default instance is an instance of the class that is provided by the runtime and does not need to be declared and instantiated using the `Dim` and `New` statements. The following example demonstrates how you might have declared and instantiated an instance of a <xref:System.Windows.Forms.Form?qualifyHint=False> class called `Form1`, and how you are now able to get a default instance of this <xref:System.Windows.Forms.Form?qualifyHint=False> class through `My.Forms`.  
  
 [!CODE [VbVbcnMy#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMy#5)]  
  
 [!CODE [VbVbcnMy#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMy#6)]  
  
 The `My.Forms` object returns a collection of default instances for every `Form` class that exists in your project. Similarly, `My.WebServices` provides a default instance of the proxy class for every Web service that you have created a reference to in your application.  
  
## See Also  
 [My.Forms Object](../Topic/My.Forms%20Object.md)   
 [My.WebServices Object](../Topic/My.WebServices%20Object.md)   
 [How My Depends on Project Type](../Topic/How%20My%20Depends%20on%20Project%20Type%20\(Visual%20Basic\).md)