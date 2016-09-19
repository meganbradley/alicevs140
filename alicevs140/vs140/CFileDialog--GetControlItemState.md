---
title: "CFileDialog::GetControlItemState"
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
ms.assetid: 7589cc8a-94e6-4dc0-bdbb-45a14fa2e04a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetControlItemState
Retrieves the current state of an item in a container control found in the dialog.  
  
## Syntax  
  
```  
HRESULT GetControlItemState(  
   DWORD dwIDCtl,  
   DWORD dwIDItem,  
   CDCONTROLSTATEF& dwState  
);  
```  
  
#### Parameters  
 `dwIDCtl`  
 The ID of the container control.  
  
 `dwIDItem`  
 The ID of the item.  
  
 `dwState`  
 A reference to a variable that receives one of more values from the CDCONTROLSTATE enumeration that indicates the current state of the control.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)