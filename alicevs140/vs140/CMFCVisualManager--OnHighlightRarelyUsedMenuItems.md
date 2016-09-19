---
title: "CMFCVisualManager::OnHighlightRarelyUsedMenuItems"
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
ms.assetid: eb578291-30fe-4d99-8bb7-6193e5c1210a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnHighlightRarelyUsedMenuItems
The framework calls this method when it draws a highlighted menu command.  
  
## Syntax  
  
```  
virtual void OnHighlightRarelyUsedMenuItems(  
   CDC* pDC,  
   CRect rectRarelyUsed  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectRarelyUsed`  
 A rectangle that specifies the boundaries of the highlighted command.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of highlighted menu commands.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)