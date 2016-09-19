---
title: "CMFCRibbonEdit::OnKey"
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
ms.assetid: 6c388fe9-3801-4ad8-860a-85ed84e89b2d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::OnKey
Called by the framework when the user presses a keytip and the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control has the focus.  
  
## Syntax  
  
```  
virtual BOOL OnKey(  
   BOOL bIsMenuKey  
);  
```  
  
#### Parameters  
 [in] `bIsMenuKey`  
 `TRUE` if the keytip displays a pop-up menu; otherwise, `FALSE`.  
  
## Return Value  
 `TRUE` if the event was handled; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonedit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)