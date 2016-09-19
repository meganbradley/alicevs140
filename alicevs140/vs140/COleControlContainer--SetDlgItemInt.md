---
title: "COleControlContainer::SetDlgItemInt"
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
ms.assetid: 8d4cd8b8-2592-4701-a6d8-ecfb87a62ff0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::SetDlgItemInt
Sets the text of a control in a dialog box to the string representation of a specified integer value.  
  
## Syntax  
  
```  
  
      virtual void SetDlgItemInt(  
   int nID,  
   UINT nValue,  
   BOOL bSigned   
);  
```  
  
#### Parameters  
 `nID`  
 The identifier of the control.  
  
 `nValue`  
 The integer value to be displayed.  
  
 `bSigned`  
 Specifies whether the `nValue` parameter is signed or unsigned. If this parameter is **TRUE**, `nValue` is signed. If this parameter is **TRUE** and `nValue` is less than zero, a minus sign is placed before the first digit in the string. If this parameter is **FALSE**, `nValue` is unsigned.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)