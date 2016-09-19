---
title: "CMFCToolBarDateTimeCtrl::OnSize"
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
ms.assetid: b68a9fa9-7393-456d-95a1-3f98373b8616
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::OnSize
Called by the framework when the parent toolbar changes its size or position and this change causes the button to change size.  
  
## Syntax  
  
```  
virtual void OnSize(  
   int iSize  
);  
```  
  
#### Parameters  
 [in] `iSize`  
 The new width of the button, in pixels.  
  
## Remarks  
 This method overrides the default class implementation ([CMFCToolBarButton::OnSize](../vs140/CMFCToolBarButton--OnSize.md)) by updating the size and position of the internal `CMFCToolBarDateTimeCtrlImpl` object.  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnSize](../vs140/CMFCToolBarButton--OnSize.md)