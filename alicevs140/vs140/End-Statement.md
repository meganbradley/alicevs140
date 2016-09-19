---
title: "End Statement"
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
ms.assetid: 0e64467c-0f34-4aab-9ddd-43f8b9d55d90
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# End Statement
Terminates execution immediately.  
  
## Syntax  
  
```  
End  
```  
  
## Remarks  
 You can place the `End` statement anywhere in a procedure to force the entire application to stop running. `End` closes any files opened with an `Open` statement and clears all the application's variables. The application closes as soon as there are no other programs holding references to its objects and none of its code is running.  
  
> [!NOTE]
>  The `End` statement stops code execution abruptly, and does not invoke the `Dispose` or `Finalize` method, or any other Visual Basic code. Object references held by other programs are invalidated. If an `End` statement is encountered within a `Try` or `Catch` block, control does not pass to the corresponding `Finally` block.  
  
 The `Stop` statement suspends execution, but unlike `End`, it does not close any files or clear any variables, unless it is encountered in a compiled executable (.exe) file.  
  
 Because `End` terminates your application without attending to any resources that might be open, you should try to close down cleanly before using it. For example, if your application has any forms open, you should close them before control reaches the `End` statement.  
  
 You should use `End` sparingly, and only when you need to stop immediately. The normal ways to terminate a procedure ([Return Statement (Visual Basic)](../vs140/Return-Statement--Visual-Basic-.md) and [Exit Statement (Visual Basic)](../vs140/Exit-Statement--Visual-Basic-.md)) not only close down the procedure cleanly but also give the calling code the opportunity to close down cleanly. A console application, for example, can simply `Return` from the `Main` procedure.  
  
> [!IMPORTANT]
>  The `End` statement calls the <xref:System.Environment.Exit?qualifyHint=False> method of the <xref:System.Environment?qualifyHint=False> class in the <xref:System?qualifyHint=False> namespace. <xref:System.Environment.Exit?qualifyHint=False> requires that you have `UnmanagedCode` permission. If you do not, a <xref:System.Security.SecurityException?qualifyHint=False> error occurs.  
  
 When followed by an additional keyword, [End <keyword\> Statement](../vs140/End--keyword--Statement--Visual-Basic-.md) delineates the end of the definition of the appropriate procedure or block. For example, `End Function` terminates the definition of a `Function` procedure.  
  
## Example  
 The following example uses the `End` statement to terminate code execution if the user requests it.  
  
 [!CODE [VbVersHelp60Controls#64](../CodeSnippet/VS_Snippets_VBCSharp/VbVersHelp60Controls#64)]  
  
## Smart Device Developer Notes  
 This statement is not supported.  
  
## See Also  
 <xref:System.Security.Permissions.SecurityPermissionFlag?qualifyHint=False>   
 [Stop Statement (Visual Basic)](../vs140/Stop-Statement--Visual-Basic-.md)   
 [End <keyword\> Statement](../vs140/End--keyword--Statement--Visual-Basic-.md)