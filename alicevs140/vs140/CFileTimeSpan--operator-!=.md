---
title: "CFileTimeSpan::operator !="
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 07687ab7-4118-431d-8e7e-794930665744
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTimeSpan::operator !=
Compares two `CFileTimeSpan` objects for inequality.  
  
## Syntax  
  
```  
  
      bool operator!=(  
   CFileTimeSpan span   
) const throw( );  
```  
  
#### Parameters  
 `span`  
 The `CFileTimeSpan` object to be compared.  
  
## Return Value  
 Returns **true** if the item being compared is not equal to the `CFileTimeSpan` object; otherwise **false**.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTimeSpan Class](../vs140/CFileTimeSpan-Class.md)