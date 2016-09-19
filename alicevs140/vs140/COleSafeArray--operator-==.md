---
title: "COleSafeArray::operator =="
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
ms.assetid: 8a4d834b-9b99-428b-9db5-c607c4bbfc75
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::operator ==
This operator compares two arrays (**SAFEARRAY**, **VARIANT**, `COleVariant`, or `COleSafeArray` arrays) and returns nonzero if they are equal; otherwise 0.  
  
## Syntax  
  
```  
  
      BOOL operator ==(  
   const SAFEARRAY& saSrc   
) const;  
BOOL operator ==(  
   LPCSAFEARRAY pSrc   
) const;  
BOOL operator ==(  
   const COleSafeArray& saSrc   
) const;  
BOOL operator ==(  
   const VARIANT& varSrc   
) const;  
BOOL operator ==(  
   LPCVARIANT pSrc   
) const;  
BOOL operator ==(  
   const COleVariant& varSrc   
) const;  
```  
  
## Remarks  
 Two arrays are equal if they have an equal number of dimensions, equal size in each dimension, and equal element values.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)