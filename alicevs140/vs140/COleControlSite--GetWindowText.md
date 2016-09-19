---
title: "COleControlSite::GetWindowText"
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
ms.assetid: be4b9f00-b3cd-4277-a150-228998623e52
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::GetWindowText
Retrieves the current text of the control.  
  
## Syntax  
  
```  
  
      virtual void GetWindowText(  
   CString& str   
) const;  
```  
  
#### Parameters  
 `str`  
 A reference to a `CString` object that contains the current text of the control.  
  
## Remarks  
 If the control supports the Caption stock property, this value is returned. If the Caption stock property is not supported, the value for the Text property is returned.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)