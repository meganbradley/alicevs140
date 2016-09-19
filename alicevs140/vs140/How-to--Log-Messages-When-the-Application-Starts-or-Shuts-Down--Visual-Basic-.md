---
title: "How to: Log Messages When the Application Starts or Shuts Down (Visual Basic)"
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
ms.assetid: 67624d05-cddf-48b7-8c36-5c99baa4c621
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Log Messages When the Application Starts or Shuts Down (Visual Basic)
You can use the `My.Application.Log` and `My.Log` objects to log information about events that occur in your application. This example shows how to use the `My.Application.Log.WriteEntry` method with the `Startup` and `Shutdown` events to write tracing information.  
  
### To access the application's event-handler code  
  
1.  Have a project selected in **Solution Explorer**. On the **Project** menu, choose **Properties**.  
  
2.  Click the **Application** tab.  
  
3.  Click the **View Application Events** button to open the Code Editor.  
  
     This opens the ApplicationEvents.vb file.  
  
### To log messages when the application starts  
  
1.  Have the ApplicationEvents.vb file open in the Code Editor. On the **General** menu, choose **MyApplication Events**.  
  
2.  On the **Declarations** menu, choose **Startup**.  
  
     The application raises the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup?qualifyHint=False> event before the main application runs.  
  
3.  Add the `My.Application.Log.WriteEntry` method to the `Startup` event handler.  
  
     [!CODE [VbVbalrMyApplicationLog#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#1)]  
  
### To log messages when the application shuts down  
  
1.  Have the ApplicationEvents.vb file open in the Code Editor. On the **General** menu, choose **MyApplication Events**.  
  
2.  On the **Declarations** menu, choose **Shutdown**.  
  
     The application raises the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown?qualifyHint=False> event after the main application runs, but before it shuts down.  
  
3.  Add the `My.Application.Log.WriteEntry` method to the `Shutdown` event handler.  
  
     [!CODE [VbVbalrMyApplicationLog#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#2)]  
  
## Example  
 You can use the **Project Designer** to access the application events in the Code Editor. For more information, see [Application Page, Project Designer (Visual Basic)](../Topic/Application%20Page,%20Project%20Designer%20\(Visual%20Basic\).md).  
  
 [!CODE [VbVbalrMyApplicationLog#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#3)]  
  
## See Also  
 <xref:Microsoft.VisualBasic.Logging.Log?qualifyHint=True>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException?qualifyHint=False>   
 [Application Page, Project Designer (Visual Basic)](../Topic/Application%20Page,%20Project%20Designer%20\(Visual%20Basic\).md)   
 [Working with Application Logs in Visual Basic](../Topic/Working%20with%20Application%20Logs%20in%20Visual%20Basic.md)