---
title: "Variable &#39;&lt;variablename&gt;&#39; is passed by reference before it has been assigned a value (Structure Variable)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8f858dd7-db04-408e-ae67-e4ff2f0e5e30
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Variable &#39;&lt;variablename&gt;&#39; is passed by reference before it has been assigned a value (Structure Variable)
Variable '<variablename\>' is passed by reference before it has been assigned a value. A null reference exception could result at runtime. Make sure the structure or all the reference members are initialized before use  
  
 A procedure call passes a structure variable as an argument to a `ByRef` parameter before any value is assigned to the variable.  
  
 If a structure variable has never been assigned a value, each structure member holds the default value for its data type. For a reference data type, that default value is [Nothing (Visual Basic)](../Topic/Nothing%20\(Visual%20Basic\).md). Reading a reference member that has a value of `Nothing` can cause a <xref:System.NullReferenceException?qualifyHint=False> in some circumstances.  
  
 Passing an argument to a procedure `ByRef` exposes the variable underlying the argument to possible modification by the procedure.  
  
 By default, this message is a warning. For more information about hiding warnings or treating warnings as errors, please see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42108  
  
### To correct this error  
  
-   If you intend the procedure to assign values to structure members through the `ByRef` argument, and if it does not matter whether the members already hold values, then no action is necessary.  
  
-   If the logic in the procedure reads a structure member before assigning any value to it, and if the member is of a value type, then make sure that the procedure logic does not depend on whether the member holds its default value or not.  
  
-   If the logic in the procedure reads a structure member before assigning any value to it, and if the member is of a reference type, then make sure that the procedure logic can handle a value of `Nothing`. For example, it could use a [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md) to catch a <xref:System.NullReferenceException?qualifyHint=False>.  
  
## See Also  
 [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [Argument Passing By Value and By Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)   
 [ByRef](../vs140/ByRef--Visual-Basic-.md)   
 [Variable Declaration in Visual Basic](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)   
 [Structures: Your Own Data Types](../vs140/Structures--Visual-Basic-.md)   
 [Structure Statement](../Topic/Structure%20Statement.md)   
 [Troubleshooting Variables in Visual Basic](../Topic/Troubleshooting%20Variables%20in%20Visual%20Basic.md)