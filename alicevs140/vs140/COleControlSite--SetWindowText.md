---
title: "COleControlSite::SetWindowText"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 747b649a-1bad-4aa1-b9f2-ab14806d81c6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::SetWindowText
Sets the text for the control site.  
  
## Syntax  
  
```  
  
      virtual void SetWindowText(  
   LPCTSTR lpszString   
);  
```  
  
#### Parameters  
 `lpszString`  
 Pointer to a null-terminated string to be used as the new title or control text.  
  
## Remarks  
 This function first attempts to set the Caption stock property. If the Caption stock property is not supported, the Text property is set instead.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)