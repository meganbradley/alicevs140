---
title: "CComCompositeControl::CalcExtent"
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
ms.assetid: 23d6a58f-5c5e-4571-9891-8f43df69006f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCompositeControl::CalcExtent
Call this method to calculate the size in **HIMETRIC** units of the dialog resource used to host the composite control.  
  
## Syntax  
  
```  
  
      BOOL CalcExtent(  
   SIZE& size   
);  
```  
  
#### Parameters  
 `size`  
 A reference to a **SIZE** structure to be filled by this method.  
  
## Return Value  
 TRUE if the control is hosted by a dialog box; otherwise FALSE.  
  
## Remarks  
 The size is returned in the `size` parameter.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComCompositeControl Class](../vs140/CComCompositeControl-Class.md)   
 [AtlPixelToHiMetric](../vs140/AtlPixelToHiMetric.md)