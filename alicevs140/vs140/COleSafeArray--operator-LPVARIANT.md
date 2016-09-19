---
title: "COleSafeArray::operator LPVARIANT"
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
ms.assetid: 9092d494-2881-4a83-915b-03de83341d10
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::operator LPVARIANT
Call this casting operator to access the underlying **VARIANT** structure for this `COleSafeArray` object.  
  
## Syntax  
  
```  
  
operator LPVARIANT( );  
```  
  
## Remarks  
 Note that changing the value in the **VARIANT** structure accessed by the pointer returned by this function will change the value of this `COleSafeArray` object.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)