---
title: "Constructor call is valid only as the first statement in an instance constructor"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c51b172f-fbd7-4ef5-8276-01a4bf6ed35b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Constructor call is valid only as the first statement in an instance constructor
A call to `New()` occurs after the first statement of a constructor. If one constructor calls another explicitly, it must do so in the first statement following the `Sub New()` statement.  
  
 **Error ID:** BC30282  
  
### To correct this error  
  
-   Remove the call to `New()`, or move it to the beginning of the constructor.  
  
## See Also  
 [NOT IN BUILD: Using Constructors and Destructors](assetId:///548eebe1-86c4-4377-b2f5-447cb8be3d90)