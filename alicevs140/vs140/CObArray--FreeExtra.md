---
title: "CObArray::FreeExtra"
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
ms.assetid: 2d9f19cb-9a3b-4da4-9a74-8e7149e56e36
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::FreeExtra
Frees any extra memory that was allocated while the array was grown.  
  
## Syntax  
  
```  
  
void FreeExtra( );  
```  
  
## Remarks  
 This function has no effect on the size or upper bound of the array.  
  
 The following table shows other member functions that are similar to `CObArray::FreeExtra`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**void FreeExtra( );**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**void FreeExtra( );**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**void FreeExtra( );**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**void FreeExtra( );**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**void FreeExtra( );**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**void FreeExtra( );**|  
  
## Example  
 See the example for [CObArray::GetData](../vs140/CObArray--GetData.md).  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)