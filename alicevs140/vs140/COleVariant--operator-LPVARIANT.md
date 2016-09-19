---
title: "COleVariant::operator LPVARIANT"
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
ms.assetid: 78690bd0-0f1d-49c1-a6b0-88515ed2ffac
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleVariant::operator LPVARIANT
Call this casting operator to access the underlying `VARIANT` structure for this `COleVariant` object.  
  
## Syntax  
  
```  
  
operator LPVARIANT( );  
  
```  
  
## Remarks  
  
> [!CAUTION]
>  Changing the value in the **VARIANT** structure accessed by the pointer returned by this function will change the value of this `COleVariant` object.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleVariant Class](../vs140/COleVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleVariant::operator LPCVARIANT](../vs140/COleVariant--operator-LPCVARIANT.md)