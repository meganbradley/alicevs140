---
title: "CComControlBase::GetZoomInfo"
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
ms.assetid: c1b6e20f-f654-4354-86eb-1586e229b4fd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetZoomInfo
Retrieves the x and y values of the numerator and denominator of the zoom factor for a control activated for in-place editing.  
  
## Syntax  
  
```  
  
      void GetZoomInfo(  
   ATL_DRAWINFO& di  
);  
```  
  
#### Parameters  
 `di`  
 The structure that will hold the zoom factor's numerator and denominator. For more information, see [ATL_DRAWINFO](../vs140/ATL_DRAWINFO-Structure.md).  
  
## Remarks  
 The zoom factor is the proportion of the control's natural size to its current extent.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)