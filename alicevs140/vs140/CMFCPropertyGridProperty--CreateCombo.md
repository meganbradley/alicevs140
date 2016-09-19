---
title: "CMFCPropertyGridProperty::CreateCombo"
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
ms.assetid: ea31b3d8-9db9-4492-816b-7d840f616e77
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::CreateCombo
Called by the framework to add a combo box to a property.  
  
## Syntax  
  
```  
virtual CComboBox* CreateCombo(  
   CWnd* pWndParent,  
   CRect rect   
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 Pointer to the parent window of the combo box.  
  
 [in] `rect`  
 The bounding rectangle of the combo box.  
  
## Return Value  
 Pointer to a new [CComboBox](../vs140/CComboBox-Class.md) object.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)