---
title: "CMFCColorBar::OnKey"
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
ms.assetid: 1ee57fae-c2c9-44a2-b65d-92c837526023
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::OnKey
Called by the framework when a user presses a keyboard button.  
  
## Syntax  
  
```  
virtual BOOL OnKey(  
   UINT nChar   
);  
```  
  
#### Parameters  
 [in] `nChar`  
 The virtual-key code for the key that a user pressed.  
  
## Return Value  
 `TRUE` if this method processes the specified key; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)