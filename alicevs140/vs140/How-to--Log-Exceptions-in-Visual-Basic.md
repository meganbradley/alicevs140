---
title: "How to: Log Exceptions in Visual Basic"
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
ms.assetid: a26c60e2-ae39-444a-aebb-33eccadc0eeb
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Log Exceptions in Visual Basic
You can use the `My.Application.Log` and `My.Log` objects to log information about exceptions that occur in your application. These examples show how to use the `My.Application.Log.WriteException` method to log exceptions that you catch explicitly and exceptions that are unhandled.  
  
 For logging tracing information, use the `My.Application.Log.WriteEntry` method. For more information, see <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry?qualifyHint=False>  
  
### To log a handled exception  
  
1.  Create the method that will generate the exception information.  
  
     [!CODE [VbVbalrMyApplicationLog#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#9)]  
  
2.  Use a `Try...Catch` block to catch the exception.  
  
     [!CODE [VbVbalrMyApplicationLog#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#6)]  
  
3.  Put the code that could generate an exception in the `Try` block.  
  
     Uncomment the `Dim` and `MsgBox` lines to cause a <xref:System.NullReferenceException?qualifyHint=False> exception.  
  
     [!CODE [VbVbalrMyApplicationLog#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#7)]  
  
4.  In the `Catch` block, use the `My.Application.Log.WriteException` method to write the exception information.  
  
     [!CODE [VbVbalrMyApplicationLog#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#8)]  
  
     The following example shows the complete code for logging a handled exception.  
  
     [!CODE [VbVbalrMyApplicationLog#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#10)]  
  
### To log an unhandled exception  
  
1.  Have a project selected in **Solution Explorer**. On the **Project** menu, choose **Properties**.  
  
2.  Click the **Application** tab.  
  
3.  Click the **View Application Events** button to open the Code Editor.  
  
     This opens the ApplicationEvents.vb file.  
  
4.  Have the ApplicationEvents.vb file open in the Code Editor. On the **General** menu, choose **MyApplication Events**.  
  
5.  On the **Declarations** menu, choose **UnhandledException**.  
  
     The application raises the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException?qualifyHint=False> event before the main application runs.  
  
6.  Add the `My.Application.Log.WriteException` method to the `UnhandledException` event handler.  
  
     [!CODE [VbVbalrMyApplicationLog#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#4)]  
  
     The following example shows the complete code for logging an unhandled exception.  
  
     [!CODE [VbVbalrMyApplicationLog#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#5)]  
  
## See Also  
 <xref:Microsoft.VisualBasic.Logging.Log?qualifyHint=True>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException?qualifyHint=False>   
 [Working with Application Logs in Visual Basic](../Topic/Working%20with%20Application%20Logs%20in%20Visual%20Basic.md)   
 [How to: Write Log Messages](../Topic/How%20to:%20Write%20Log%20Messages%20\(Visual%20Basic\).md)   
 [Walkthrough: Determining Where My.Application.Log Writes Information](../Topic/Walkthrough:%20Determining%20Where%20My.Application.Log%20Writes%20Information%20\(Visual%20Basic\).md)   
 [Walkthrough: Changing Where My.Application.Log Writes Information](../vs140/Walkthrough--Changing-Where-My.Application.Log-Writes-Information--Visual-Basic-.md)