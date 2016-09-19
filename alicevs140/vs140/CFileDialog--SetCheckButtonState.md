---
title: "CFileDialog::SetCheckButtonState"
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
ms.assetid: e61d8070-f774-4f6e-a272-294c47dfc057
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::SetCheckButtonState
Sets the current state of a check button (check box) in the dialog.  
  
## Syntax  
  
```  
HRESULT SetCheckButtonState(  
   DWORD dwIDCtl,  
   BOOL bChecked  
);  
```  
  
#### Parameters  
 `dwIDCtl`  
 The ID of the check box.  
  
 `bChecked`  
 The state of the check box. `TRUE` indicates checked; `FALSE` indicates Unchecked.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)