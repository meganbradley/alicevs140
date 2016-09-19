---
title: "Invalid pattern string"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ec1aecdb-5339-4a93-be71-eec56b1d7438
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Invalid pattern string
The pattern string specified in the `Like` operation of a search is invalid.  
  
### To correct this error  
  
1.  Review the valid characters for list expressions.  
  
2.  In the pattern range, ensure that the start range character is less than the end range character, as in `[a-z]`.  
  
3.  In the pattern range, ensure that there are not multiple hyphens next to each other, as in `[a--z]`.  
  
4.  End pattern ranges with a closing bracket.  
  
## See Also  
 [Like Operator](../vs140/Like-Operator--Visual-Basic-.md)