---
title: "CMFCVisualManager::OnFillOutlookBarCaption"
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
ms.assetid: b16b18c0-6987-4890-83af-d1fb0d556d98
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillOutlookBarCaption
The framework calls this method when it fills the background of an Outlook caption bar.  
  
## Syntax  
  
```  
virtual void OnFillOutlookBarCaption(  
   CDC* pDC,  
   CRect rectCaption,  
   COLORREF& clrText  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectCaption`  
 A rectangle that specifies the boundaries of the caption bar.  
  
 [out] `clrText`  
 A reference to a [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) parameter. The method writes the color of text on the caption bar to this parameter.  
  
## Remarks  
 The default implementation of this method fills the caption bar with the color for shadows based on the current skin. Override this method in a derived visual manager to customize the color of the Outlook caption bar.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)