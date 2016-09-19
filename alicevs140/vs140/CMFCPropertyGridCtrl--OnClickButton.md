---
title: "CMFCPropertyGridCtrl::OnClickButton"
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
ms.assetid: e079bd77-6796-4872-998f-29bd16cddc35
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::OnClickButton
Called by the framework when a property button is clicked.  
  
## Syntax  
  
```  
virtual void OnClickButton(  
   CPoint point   
);  
```  
  
#### Parameters  
 [in] `point`  
 A point, in client coordinates.  
  
## Remarks  
 By default, this method updates the current property value.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)