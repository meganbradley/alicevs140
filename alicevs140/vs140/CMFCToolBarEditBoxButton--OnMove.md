---
title: "CMFCToolBarEditBoxButton::OnMove"
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
ms.assetid: 0aa69f08-147f-4c68-b580-200a39ba97c7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::OnMove
Called by the framework when the parent toolbar moves.  
  
## Syntax  
  
```  
virtual void OnMove();  
```  
  
## Remarks  
 This method overrides the default class implementation ([CMFCToolBarButton::OnMove](../vs140/CMFCToolBarButton--OnMove.md)) by updating the position of the internal `CEdit` object  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnMove](../vs140/CMFCToolBarButton--OnMove.md)   
 [CEdit Class](../vs140/CEdit-Class.md)