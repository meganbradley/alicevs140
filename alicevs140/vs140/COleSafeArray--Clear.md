---
title: "COleSafeArray::Clear"
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
ms.assetid: 7281edf1-b50d-48ce-aa8d-f8f60e512021
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::Clear
Clears the safe array.  
  
## Syntax  
  
```  
  
void Clear( );  
```  
  
## Remarks  
 The function clears a safe array by setting the `VARTYPE` of the object to `VT_EMPTY`. The current contents are released and the array is freed.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)