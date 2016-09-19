---
title: "No mouse is present"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4472fd57-4217-4463-9d3c-dc4a8fe88f1b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# No mouse is present
One of the properties of the `My.Computer.Mouse` object was called, but the computer has no mouse or mouse port installed.  
  
### To correct this error  
  
-   Add a `Try...Catch` block around the call to the property of the `My.Computer.Mouse` object.  
  
     — or —  
  
-   Install a mouse on the computer.  
  
## See Also  
 [My.Computer.Mouse Object](../Topic/My.Computer.Mouse%20Object.md)   
 [Exception and Error Handling in Visual Basic](assetId:///3e351e73-cf23-40ab-8b60-05794160529e)   
 [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)