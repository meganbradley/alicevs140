---
title: "&#39;Optional&#39; expected"
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
ms.assetid: 6f75060c-2db4-4a79-b5d1-5780c09a74cd
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Optional&#39; expected
An optional argument in a procedure declaration is followed by a required argument. Every argument following an optional argument must also be optional.  
  
 **Error ID:** BC30202  
  
### To correct this error  
  
1.  If the argument is intended to be required, move it to precede the first optional argument in the argument list.  
  
2.  If the argument is intended to be optional, use the `Optional` keyword.  
  
## See Also  
 [Optional Parameters](../vs140/Optional-Parameters--Visual-Basic-.md)