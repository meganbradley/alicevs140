---
title: "CMFCPropertyGridCtrl::OnDrawProperty"
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
ms.assetid: 1a315f83-5062-4d83-a404-4c929ddbf788
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::OnDrawProperty
Called by the framework to display a property.  
  
## Syntax  
  
```  
virtual int OnDrawProperty(  
   CDC* pDC,  
   CMFCPropertyGridProperty* pProp   
) const;  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pProp`  
 A pointer to a property object.  
  
## Return Value  
 `TRUE` if this method is successful; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)