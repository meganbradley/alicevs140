---
title: "&#39;&lt;procedurename1&gt;&#39; cannot override &#39;&lt;procedurename2&gt;&#39; because it is not accessible in this context"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1a36acbf-cead-43a0-b12f-f52f94d09124
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;procedurename1&gt;&#39; cannot override &#39;&lt;procedurename2&gt;&#39; because it is not accessible in this context
A procedure or property overrides a procedure or property with an access level that prevents access by the overriding procedure or property.  
  
 For example, if a procedure is declared as `Friend` in one assembly, it cannot be accessed outside that assembly. If a procedure in another assembly in the same project attempts to override the `Friend` procedure, it cannot access it to override it.  
  
 **Error ID:** BC31417  
  
### To correct this error  
  
-   Move the overriding procedure or property to the same assembly as the procedure or property it is to override.  
  
     -or-  
  
-   Remove the `Overrides` keyword.  
  
## See Also  
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)   
 [Overrides](../vs140/Overrides--Visual-Basic-.md)   
 [NOT IN BUILD: Overriding Properties and Methods](assetId:///2167e8f5-1225-4b13-9ebd-02591ba90213)