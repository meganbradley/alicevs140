---
title: "CFileDialog::GetControlState"
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
ms.assetid: 39881e39-aaa0-403c-9939-39eed5fae2c3
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetControlState
Retrieves the current visibility and enabled states of a given control.  
  
## Syntax  
  
```  
HRESULT GetControlState(  
   DWORD dwIDCtl,  
   CDCONTROLSTATEF& dwState  
);  
```  
  
#### Parameters  
 `dwIDCtl`  
 The ID of the control.  
  
 `dwState`  
 A reference to a variable that receives one or more values from the CDCONTROLSTATE enumeration that indicates the current state of the control.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)