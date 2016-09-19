---
title: "CMFCCaptionBar::OnDrawText"
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
ms.assetid: 67440963-2f89-4d9f-8538-ce26fb6698a3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCaptionBar::OnDrawText
Called by the framework to draw the caption bar text.  
  
## Syntax  
  
```  
virtual void OnDrawText(  
   CDC* pDC,  
   CRect rect,  
   const CString& strText   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context that is used to display the button.  
  
 [in] `rect`  
 The bounding rectangle of the text.  
  
 [in] `strText`  
 The text string to display.  
  
## Remarks  
 The default implementation displays the text by using `CDC::DrawText` and [CMFCCaptionBar::m_clrBarText](../vs140/CMFCCaptionBar--m_clrBarText.md) color.  
  
 Override this method in a `CMFCCaptionBar` derived class to customize the appearance of the caption bar's text.  
  
## Requirements  
 **Header:** afxcaptionbar.h  
  
## See Also  
 [CMFCCaptionBar Class](../vs140/CMFCCaptionBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)