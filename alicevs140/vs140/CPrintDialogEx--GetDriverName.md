---
title: "CPrintDialogEx::GetDriverName"
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
ms.assetid: 5b1994e3-5cde-4f12-bee0-31b086154908
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::GetDriverName
Call this function after calling [DoModal](../vs140/CPrintDialogEx--DoModal.md) or [GetDefaults](../vs140/CPrintDialogEx--GetDefaults.md) to retrieve the name of the system-defined printer device driver.  
  
## Syntax  
  
```  
  
CString GetDriverName( ) const;  
  
```  
  
## Return Value  
 A `CString` specifying the system-defined driver name.  
  
## Remarks  
 Use a pointer to the `CString` object returned by `GetDriverName` as the value of `lpszDriverName` in a call to [CDC::CreateDC](../vs140/CDC--CreateDC.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::GetDeviceName](../vs140/CPrintDialogEx--GetDeviceName.md)   
 [CPrintDialogEx::GetDevMode](../vs140/CPrintDialogEx--GetDevMode.md)   
 [CPrintDialogEx::GetPortName](../vs140/CPrintDialogEx--GetPortName.md)