---
title: "CFileDialog::SetSelectedControlItem"
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
ms.assetid: aa5b26cc-7ed5-4f8b-b540-253e58939587
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::SetSelectedControlItem
Sets the selected state of a particular item in an option button group or a combo box found in the dialog.  
  
## Syntax  
  
```  
HRESULT SetSelectedControlItem(  
   DWORD dwIDCtl,  
   DWORD dwIDItem  
);  
```  
  
#### Parameters  
 `dwIDCtl`  
 The ID of the container control.  
  
 `dwIDItem`  
 The ID of the item that the user selected in the control.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)