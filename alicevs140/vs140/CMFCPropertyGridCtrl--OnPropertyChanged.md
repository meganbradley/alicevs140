---
title: "CMFCPropertyGridCtrl::OnPropertyChanged"
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
ms.assetid: 52afbf02-96c3-41ad-9566-3f053f5c4991
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::OnPropertyChanged
Called by the framework when the value of a property is changed.  
  
## Syntax  
  
```  
virtual void OnPropertyChanged(  
   CMFCPropertyGridProperty* pProp   
) const;  
```  
  
#### Parameters  
 [in] `pProp`  
 A pointer to a property object whose value has changed.  
  
## Remarks  
 By default, this method sends the [AFX_WM_PROPERTY_CHANGED](../vs140/AFX-Messages.md) message to the owner of the property grid control.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [AFX Messages](../vs140/AFX-Messages.md)