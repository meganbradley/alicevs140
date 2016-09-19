---
title: "CPrintDialogEx::GetDeviceName"
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
ms.assetid: d30300b7-85a9-49d3-acc0-73fef102bb8c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::GetDeviceName
Call this function after calling [DoModal](../vs140/CPrintDialogEx--DoModal.md) to retrieve the name of the currently selected printer, or after calling [GetDefaults](../vs140/CPrintDialogEx--GetDefaults.md) to retrieve the name of the default printer.  
  
## Syntax  
  
```  
  
CString GetDeviceName( ) const;  
  
```  
  
## Return Value  
 The name of the currently selected printer.  
  
## Remarks  
 Use a pointer to the `CString` object returned by `GetDeviceName` as the value of `lpszDeviceName` in a call to [CDC::CreateDC](../vs140/CDC--CreateDC.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::GetDriverName](../vs140/CPrintDialogEx--GetDriverName.md)   
 [CPrintDialogEx::GetDevMode](../vs140/CPrintDialogEx--GetDevMode.md)   
 [CPrintDialogEx::GetPortName](../vs140/CPrintDialogEx--GetPortName.md)