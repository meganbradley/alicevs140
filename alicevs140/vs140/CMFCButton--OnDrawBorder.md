---
title: "CMFCButton::OnDrawBorder"
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
ms.assetid: f146e90c-85d6-42e5-87c1-0c5c2be7b71e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::OnDrawBorder
Called by the framework to draw the border of a button.  
  
## Syntax  
  
```  
virtual void OnDrawBorder(  
   CDC* pDC,  
   CRect& rectClient,  
   UINT uiState   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectClient`  
 A reference to a rectangle that bounds the button.  
  
 [in] `uiState`  
 The current button state. For more information, see the `itemState` member of the [DRAWITEMSTRUCT Structure](../vs140/DRAWITEMSTRUCT-Structure.md) topic.  
  
## Remarks  
 Override this method to use your own code to draw the border.  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)