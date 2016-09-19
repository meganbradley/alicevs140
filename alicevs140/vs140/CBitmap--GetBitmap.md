---
title: "CBitmap::GetBitmap"
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
ms.assetid: 0ae87099-cbdd-4a97-a431-f0633a622d3b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBitmap::GetBitmap
Retrieves image properties for the attached bitmap.  
  
## Syntax  
  
```  
int GetBitmap(  
   BITMAP* pBitMap  
);  
```  
  
#### Parameters  
 `pBitMap`  
 Pointer to a [BITMAP Structure](../vs140/BITMAP-Structure.md) structure that will receive the image properties. This parameter must not be `NULL`.  
  
## Return Value  
 Nonzero if the method was successful; otherwise 0.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CBitmap Class](../vs140/CBitmap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [BITMAP Structure](../vs140/BITMAP-Structure.md)