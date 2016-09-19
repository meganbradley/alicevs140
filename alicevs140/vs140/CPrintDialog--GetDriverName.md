---
title: "CPrintDialog::GetDriverName"
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
ms.assetid: e9e3878b-7940-45c5-8f20-485bbdf34fc2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::GetDriverName
Retrieves the name of the currently selected printer driver.  
  
## Syntax  
  
```  
  
CString GetDriverName( ) const;  
```  
  
## Return Value  
 A `CString` specifying the system-defined driver name.  
  
## Remarks  
 Call this function after calling [DoModal](../vs140/CPrintDialog--DoModal.md) or [GetDefaults](../vs140/CPrintDialog--GetDefaults.md) to retrieve the name of the system-defined printer device driver. Use a pointer to the `CString` object returned by `GetDriverName` as the value of `lpszDriverName` in a call to [CDC::CreateDC](../vs140/CDC--CreateDC.md).  
  
## Example  
 See the example for [CPrintDialog::GetDeviceName](../vs140/CPrintDialog--GetDeviceName.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::GetDeviceName](../vs140/CPrintDialog--GetDeviceName.md)   
 [CPrintDialog::GetDevMode](../vs140/CPrintDialog--GetDevMode.md)   
 [CPrintDialog::GetPortName](../vs140/CPrintDialog--GetPortName.md)