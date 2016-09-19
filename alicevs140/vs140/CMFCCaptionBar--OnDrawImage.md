---
title: "CMFCCaptionBar::OnDrawImage"
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
ms.assetid: b7ca7642-d08f-4951-9d92-1e09c78d2328
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCaptionBar::OnDrawImage
Called by the framework to draw the caption bar image.  
  
## Syntax  
  
```  
virtual void OnDrawImage(  
   CDC* pDC,  
   CRect rect   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context that is used to display the image.  
  
 [in] `rect`  
 Specifies the bounding rectangle of the image.  
  
## Remarks  
 Override this method in a `CMFCCaptionBar` derived class to customize the image appearance.  
  
## Requirements  
 **Header:** afxcaptionbar.h  
  
## See Also  
 [CMFCCaptionBar Class](../vs140/CMFCCaptionBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)