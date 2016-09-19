---
title: "CMFCPropertyGridCtrl::OnDrawDescription"
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
ms.assetid: 6b1a53f9-5c95-4478-bd78-7507589b9e1a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::OnDrawDescription
Called by the framework to draw the description area and display the description text.  
  
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
 A rectangle that specifies where to draw the description area.  
  
## Remarks  
 Use the [CMFCPropertyGridCtrl::EnableDescriptionArea](../vs140/CMFCPropertyGridCtrl--EnableDescriptionArea.md) method to display the description area.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridCtrl::EnableDescriptionArea](../vs140/CMFCPropertyGridCtrl--EnableDescriptionArea.md)