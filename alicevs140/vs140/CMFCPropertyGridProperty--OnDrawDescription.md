---
title: "CMFCPropertyGridProperty::OnDrawDescription"
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
ms.assetid: c9afbf2d-fe82-48bc-898a-b2751116719a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::OnDrawDescription
Called by the framework to draw the property description.  
  
## Syntax  
  
```  
virtual void OnDrawDescription(  
   CDC* pDC,  
   CRect rect   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A bounding rectangle that specifies where to draw the property description.  
  
## Remarks  
 By default, this method draws the property name and description in the font used by the parent property list control. The property description is drawn in regular style and the property name is drawn in bold style.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)