---
title: "CMFCButton::OnFillBackground"
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
ms.assetid: d6edb142-ad05-4715-8112-4366d51dc26e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::OnFillBackground
Called by the framework to draw the background of the button text.  
  
## Syntax  
  
```  
virtual void OnFillBackground(  
   CDC* pDC,  
   const CRect& rectClient   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectClient`  
 A reference to a rectangle that bounds the button.  
  
## Remarks  
 Override this method to use your own code to draw the background of a button.  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)