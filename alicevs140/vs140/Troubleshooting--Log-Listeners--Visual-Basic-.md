---
title: "Troubleshooting: Log Listeners (Visual Basic)"
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
ms.assetid: ac6eb760-3d5d-461e-aedd-40599ee22e49
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting: Log Listeners (Visual Basic)
You can use the `My.Application.Log` and `My.Log` objects to log information about events that occur in your application.  
  
 To determine which log listeners receive those messages, see [Walkthrough: Determining Where My.Application.Log Writes Information](../Topic/Walkthrough:%20Determining%20Where%20My.Application.Log%20Writes%20Information%20\(Visual%20Basic\).md).  
  
 The `Log` object can use log filtering to limit the amount of information that it logs. If the filters are misconfigured, the logs might contain the wrong information. For more information about filtering, see [Walkthrough: Filtering My.Application.Log Output](../Topic/Walkthrough:%20Filtering%20My.Application.Log%20Output%20\(Visual%20Basic\).md).  
  
 However, if a log is configured incorrectly, you may need more information about its current configuration. You can get to this information through the log's advanced `TraceSource` property.  
  
### To determine the log listeners for the Log object in code  
  
1.  Import the <xref:System.Diagnostics?qualifyHint=False> namespace at the beginning of the code file. For more information, see [Imports Statement](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md).  
  
     [!CODE [VbVbalrMyApplicationLog#13](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#13)]  
  
2.  Create a function that returns a string consisting of information for each of the log's listeners.  
  
     [!CODE [VbVbalrMyApplicationLog#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#14)]  
  
3.  Pass the collection of the log's trace listeners to the `GetListeners` function, and display the return value.  
  
     [!CODE [VbVbalrMyApplicationLog#19](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#19)]  
  
     For more information, see <xref:Microsoft.VisualBasic.Logging.Log.TraceSource?qualifyHint=False>.  
  
## See Also  
 <xref:Microsoft.VisualBasic.Logging.Log?qualifyHint=True>   
 [Working with Application Logs in Visual Basic](../Topic/Working%20with%20Application%20Logs%20in%20Visual%20Basic.md)   
 [Walkthrough: Determining Where My.Application.Log Writes Information](../Topic/Walkthrough:%20Determining%20Where%20My.Application.Log%20Writes%20Information%20\(Visual%20Basic\).md)