---
title: "CMFCCaptionBar::OnDrawBackground"
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
ms.assetid: 5f0ec026-42e8-4dc0-8113-c6ee28b8328b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCaptionBar::OnDrawBackground
Called by the framework to fill the background of the caption bar.  
  
## Syntax  
  
```  
virtual void OnDrawBackground(  
   CDC* pDC,  
   CRect rect   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to the device context of the caption bar.  
  
 [in] `rect`  
 The bounding rectangle to fill.  
  
## Remarks  
 The `OnDrawBackground` method is called when the background of the caption bar is about to be filled. The default implementation fills the background by using the [CMFCCaptionBar::m_clrBarBackground](../vs140/CMFCCaptionBar--m_clrBarBackground.md) color.  
  
 Override this method in a `CMFCCaptionBar` derived class to customize the appearance of the caption bar.  
  
## Requirements  
 **Header:** afxcaptionbar.h  
  
## See Also  
 [CMFCCaptionBar Class](../vs140/CMFCCaptionBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)