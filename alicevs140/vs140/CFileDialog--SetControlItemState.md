---
title: "CFileDialog::SetControlItemState"
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
ms.assetid: 0cb59ed1-71da-4526-8004-e44c0df5dd81
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::SetControlItemState
Sets the current state of an item in a container control found in the dialog.  
  
## Syntax  
  
```  
HRESULT SetControlItemState(  
   DWORD dwIDCtl,  
   DWORD dwIDItem,  
   CDCONTROLSTATEF dwState  
);  
```  
  
#### Parameters  
 `dwIDCtl`  
 The ID of the container control.  
  
 `dwIDItem`  
 The ID of the item.  
  
 `dwState`  
 One or more values from the CDCONTROLSTATE enumeration that indicate the new state of the control.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)