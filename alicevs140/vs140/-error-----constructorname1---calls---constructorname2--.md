---
title: "&lt;error&gt;: &#39;&lt;constructorname1&gt;&#39; calls &#39;&lt;constructorname2&gt;&#39;"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dfca67d7-f4d7-4451-a937-68f22b8527d5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;error&gt;: &#39;&lt;constructorname1&gt;&#39; calls &#39;&lt;constructorname2&gt;&#39;
A circular constructor call occurs. A constructor makes a call to `Me.New()` or `MyClass.New()`. One possible cause is an attempt to call an overloaded constructor with a different argument list.  
  
 **Error ID:** BC30297  
  
### To correct this error  
  
-   Use a different argument list to call an overloaded constructor.  
  
-   If there are no accessible overloads, remove the call to `Me.New()` or `MyClass.New()`.  
  
## See Also  
 [NOT IN BUILD: Using Constructors and Destructors](assetId:///548eebe1-86c4-4377-b2f5-447cb8be3d90)