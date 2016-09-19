---
title: "CWnd::SetDlgItemInt"
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
ms.assetid: 1c5d30e9-4722-41f5-8bd1-b2023c569379
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetDlgItemInt
Sets the text of a given control in a dialog box to the string representation of a specified integer value.  
  
## Syntax  
  
```  
  
      void SetDlgItemInt(  
   int nID,  
   UINT nValue,  
   BOOL bSigned = TRUE   
);  
```  
  
#### Parameters  
 `nID`  
 Specifies the integer ID of the control to be changed.  
  
 `nValue`  
 Specifies the integer value used to generate the item text.  
  
 `bSigned`  
 Specifies whether the integer value is signed or unsigned. If this parameter is **TRUE**, `nValue` is signed. If this parameter is **TRUE** and `nValue` is less than 0, a minus sign is placed before the first digit in the string. If this parameter is **FALSE**, `nValue` is unsigned.  
  
## Remarks  
 `SetDlgItemInt` sends a [WM_SETTEXT](http://msdn.microsoft.com/library/windows/desktop/ms632644) message to the given control.  
  
## Example  
 See the example for [CWnd::SetDlgItemText](../vs140/CWnd--SetDlgItemText.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDlgItemInt](../vs140/CWnd--GetDlgItemInt.md)   
 [SetDlgItemInt](http://msdn.microsoft.com/library/windows/desktop/ms645518)   
 [WM_SETTEXT](http://msdn.microsoft.com/library/windows/desktop/ms632644)