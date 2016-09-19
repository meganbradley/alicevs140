---
title: "CFileDialog::GetSelectedControlItem"
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
ms.assetid: e841adff-6e26-45b2-9a09-e1eaedeb9d50
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetSelectedControlItem
Retrieves a particular item from the specified container control in the dialog.  
  
## Syntax  
  
```  
HRESULT GetSelectedControlItem(  
   DWORD dwIDCtl,  
   DWORD& dwIDItem  
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