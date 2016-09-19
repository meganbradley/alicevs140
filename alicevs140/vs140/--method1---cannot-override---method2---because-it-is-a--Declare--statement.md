---
title: "&#39;&lt;method1&gt;&#39; cannot override &#39;&lt;method2&gt;&#39; because it is a &#39;Declare&#39; statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7277e8cc-aa3c-40c3-8682-c8c42d2ee921
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;method1&gt;&#39; cannot override &#39;&lt;method2&gt;&#39; because it is a &#39;Declare&#39; statement
You attempted to override a delegate on the base class name that was declared with a `Declare` statement.  
  
 **Error ID:** BC30474  
  
### To correct this error  
  
1.  Change the overridden member so it is not a `Declare` statement.  
  
2.  Do not try to override this method.  
  
## See Also  
 [Declare Statement](../Topic/Declare%20Statement.md)   
 [NOT IN BUILD: Overriding Properties and Methods](assetId:///2167e8f5-1225-4b13-9ebd-02591ba90213)