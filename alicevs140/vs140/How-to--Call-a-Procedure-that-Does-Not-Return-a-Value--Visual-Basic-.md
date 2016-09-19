---
title: "How to: Call a Procedure that Does Not Return a Value (Visual Basic)"
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
ms.assetid: 259b49a3-a3c1-4254-ba8c-73cdc4127703
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Call a Procedure that Does Not Return a Value (Visual Basic)
A `Sub` procedure does not return a value to the calling code. You call it explicitly with a stand-alone calling statement. You cannot call it by simply using its name within an expression.  
  
### To call a Sub procedure  
  
1.  Specify the name of the `Sub` procedure.  
  
2.  Follow the procedure name with parentheses to enclose the argument list. If there are no arguments, you can optionally omit the parentheses. However, using the parentheses makes your code easier to read.  
  
3.  Place the arguments in the argument list within the parentheses, separated by commas. Be sure you supply the arguments in the same order that the `Sub` procedure defines the corresponding parameters.  
  
     The following example calls the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] <xref:Microsoft.VisualBasic.Interaction.AppActivate?qualifyHint=False> function to activate an application window. <xref:Microsoft.VisualBasic.Interaction.AppActivate?qualifyHint=False> takes the window title as its sole argument. It does not return a value to the calling code. If a Notepad process is not running, the example throws an <xref:System.ArgumentException?qualifyHint=False>. The `Shell` procedure assumes the applications are in the paths specified.  
  
     [!CODE [VbVbalrCatRef#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCatRef#11)]  
  
## See Also  
 <xref:Microsoft.VisualBasic.Interaction.Shell?qualifyHint=False>   
 <xref:System.ArgumentException?qualifyHint=False>   
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)   
 [How to: Create a Procedure](../vs140/How-to--Create-a-Procedure--Visual-Basic-.md)   
 [How to: Call a Procedure that Returns a Value](../vs140/How-to--Call-a-Procedure-That-Returns-a-Value--Visual-Basic-.md)   
 [How to: Call an Event Handler in Visual Basic](../Topic/How%20to:%20Call%20an%20Event%20Handler%20in%20Visual%20Basic.md)