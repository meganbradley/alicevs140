---
title: "&#39;Catch&#39; block never reached; &lt;exception&gt; handled above in the same &#39;Try&#39; statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7d15597c-5988-42ea-a853-63cbf78faaf3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Catch&#39; block never reached; &lt;exception&gt; handled above in the same &#39;Try&#39; statement
A `Catch` block in the code cannot be reached because it is handled in a preceding `Try` block.  
  
 By default, this message is a warning. For more information about hiding warnings or treating warnings as errors, please see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md)  
  
 **Error ID:** BC42031  
  
### To correct this error  
  
-   Remove the redundant statement.  
  
## See Also  
 [How to: Catch an Exception in Visual Basic](assetId:///f3063c89-d2bf-49b1-91b5-b87edfb18b95)   
 [How to: Test Code with a Try…Catch Block in Visual Basic](assetId:///8368e205-ed73-4185-a247-af84fb4fafa9)   
 [How to: Filter Errors in a Catch Block in Visual Basic](assetId:///85964d0a-56e7-4301-a96e-5eaea23b7b9b)   
 [Walkthrough: Structured Exception Handling (Visual Basic)](assetId:///440da655-4b32-490b-8b16-bfe46f41fa76)   
 [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)