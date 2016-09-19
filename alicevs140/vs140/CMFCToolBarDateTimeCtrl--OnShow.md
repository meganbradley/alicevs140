---
title: "CMFCToolBarDateTimeCtrl::OnShow"
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
ms.assetid: 31074a04-b2ac-4e23-b991-e6f55b34df79
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::OnShow
Called by the framework when the button becomes visible or invisible.  
  
## Syntax  
  
```  
virtual void OnShow(  
   BOOL bShow  
);  
```  
  
#### Parameters  
 [in] `bShow`  
 Specifies whether the button is visible. If this parameter is `TRUE`, the button is visible. Otherwise, the button is not visible.  
  
## Remarks  
 This method extends the base class implementation ([CMFCToolBarButton::OnShow](../vs140/CMFCToolBarButton--OnShow.md)) by displaying the button if `bShow` is `TRUE`. Otherwise, this method hides the button.  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnShow](../vs140/CMFCToolBarButton--OnShow.md)