---
title: "CPageSetupDialog::GetDriverName"
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
ms.assetid: 1f0362e1-4705-447a-8a1b-690957f3e893
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPageSetupDialog::GetDriverName
Call this function after calling [DoModal](../vs140/CPrintDialog--DoModal.md) to retrieve the name of the system-defined printer device driver.  
  
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
 [CPageSetupDialog Class](../vs140/CPageSetupDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPageSetupDialog::GetDeviceName](../vs140/CPageSetupDialog--GetDeviceName.md)   
 [CPageSetupDialog::GetDevMode](../vs140/CPageSetupDialog--GetDevMode.md)   
 [CPageSetupDialog::GetPortName](../vs140/CPageSetupDialog--GetPortName.md)