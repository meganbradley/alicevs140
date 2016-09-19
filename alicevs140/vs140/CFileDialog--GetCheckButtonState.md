---
title: "CFileDialog::GetCheckButtonState"
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
ms.assetid: c44f6dea-5a87-4701-a670-8c9393a6860c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetCheckButtonState
Retrieves the current state of a check button (check box) in the dialog.  
  
## Syntax  
  
```  
HRESULT GetCheckButtonState(  
   DWORD dwIDCtl,  
   BOOL& bChecked  
);  
```  
  
#### Parameters  
 `dwIDCtl`  
 The ID of the check box.  
  
 `bChecked`  
 The state of the check box. `TRUE` indicates checked; `FALSE` indicates unchecked.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)