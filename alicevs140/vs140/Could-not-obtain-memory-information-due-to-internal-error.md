---
title: "Could not obtain memory information due to internal error"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1ba8f774-5858-438e-914e-99fddc9e5e7e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Could not obtain memory information due to internal error
A call to one of the memory-information properties of the `My.Computer.Info` object failed.  
  
### To correct this error  
  
-   Add a `Try...Catch` block around the call to the memory-information property of the `My.Computer.Info` object.  
  
## See Also  
 [My.Computer.Info Object](../vs140/My.Computer.Info-Object.md)   
 [Exception and Error Handling in Visual Basic](assetId:///3e351e73-cf23-40ab-8b60-05794160529e)   
 [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)