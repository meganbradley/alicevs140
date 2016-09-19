---
title: "System.Diagnostics.DebuggerHiddenAttribute does not affect &#39;Get&#39; or &#39;Set&#39; when applied to the Property definition"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 623d5e48-7fb2-48a9-bbbb-92914b08c01c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# System.Diagnostics.DebuggerHiddenAttribute does not affect &#39;Get&#39; or &#39;Set&#39; when applied to the Property definition
System.Diagnostics.DebuggerHiddenAttribute does not affect 'Get' or 'Set' when applied to the Property definition. Apply the attribute directly to the 'Get' and 'Set' procedures as appropriate.  
  
 The <xref:System.Diagnostics.DebuggerHiddenAttribute?qualifyHint=False> is applied to a property declaration.  
  
 Source code can apply the <xref:System.Diagnostics.DebuggerHiddenAttribute?qualifyHint=False> to a procedure. Doing so signals the Visual Studio debugger not to stop inside the procedure and not to allow any breakpoints to be set in the procedure.  
  
 Although you can apply <xref:System.Diagnostics.DebuggerHiddenAttribute?qualifyHint=False> to a property, it does not have any effect. It has the effect that you want only if you apply it to the property's `Get` or `Set` procedure.  
  
 By default, this message is a warning. For information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40051  
  
### To correct this error  
  
-   Remove the <xref:System.Diagnostics.DebuggerHiddenAttribute?qualifyHint=False> from the property declaration and apply it to the property's `Get` or `Set` procedure as appropriate.  
  
## See Also  
 <xref:System.Diagnostics.DebuggerHiddenAttribute?qualifyHint=False>   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Property Statement](../vs140/Property-Statement.md)   
 [Get Statement](../vs140/Get-Statement.md)   
 [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md)