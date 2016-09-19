---
title: "CFileDialog::SetControlLabel"
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
ms.assetid: 7811a367-8d79-4b6e-98a7-c8db22b05aac
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::SetControlLabel
Sets the text associated with a control, such as button text or an edit box label.  
  
## Syntax  
  
```  
HRESULT SetControlLabel(  
   DWORD dwIDCtl,  
   const CString& strLabel  
);  
```  
  
#### Parameters  
 `dwIDCtl`  
 The ID of the control.  
  
 `strLabel`  
 The control name.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)