---
title: "CMFCButton::OnDraw"
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
ms.assetid: 41e5b88c-7008-40c2-8f0a-a68c4fc35f6f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::OnDraw
Called by the framework to draw a button.  
  
## Syntax  
  
```  
virtual void OnDraw(  
   CDC* pDC,  
   const CRect& rect,  
   UINT uiState   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A reference to a rectangle that bounds the button.  
  
 [in] `uiState`  
 The current button state. For more information, see the `itemState` member of the [DRAWITEMSTRUCT Structure](../vs140/DRAWITEMSTRUCT-Structure.md) topic.  
  
## Remarks  
 Override this method to use your own code to draw a button.  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)