---
title: "CMFCToolBarDateTimeCtrl::OnMove"
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
ms.assetid: 018f36a8-15a0-490a-9df5-1e9bbacca208
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::OnMove
Called by the framework when the parent toolbar moves.  
  
## Syntax  
  
```  
virtual void OnMove();  
```  
  
## Remarks  
 This method overrides the default class implementation ([CMFCToolBarButton::OnMove](../vs140/CMFCToolBarButton--OnMove.md)) by updating the position of the internal `CMFCToolBarDateTimeCtrlImpl` object.  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarDateTimeCtrlImpl Class](assetId:///4fcddcbc-b374-4c27-bfb4-09fb0ca2eac5)