---
title: "CMFCVisualManager::OnDrawOutlookPageButtonBorder"
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
ms.assetid: 0c219681-fce2-4b33-a4bd-9d0c2173f213
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawOutlookPageButtonBorder
Called by the framework when it draws the border of an Outlook page button.  
  
## Syntax  
  
```  
virtual void OnDrawOutlookPageButtonBorder(  
   CDC* pDC,  
   CRect& rectBtn,  
   BOOL bIsHighlighted,  
   BOOL bIsPressed  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectBtn`  
 A rectangle that specifies the boundary of the Outlook page button.  
  
 [in] `bIsHighlighted`  
 A Boolean that specifies whether the button is highlighted.  
  
 [in] `bIsPressed`  
 A Boolean that specifies whether the button is pressed.  
  
## Remarks  
 Override this method in a custom visual manager to change the appearance of the Outlook page button.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)