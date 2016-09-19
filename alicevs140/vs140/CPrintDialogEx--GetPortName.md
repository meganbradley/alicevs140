---
title: "CPrintDialogEx::GetPortName"
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
ms.assetid: b28d37b0-763f-4af4-a9b6-f7ce6a81eb8f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::GetPortName
Call this function after calling [DoModal](../vs140/CPrintDialogEx--DoModal.md) or [GetDefaults](../vs140/CPrintDialogEx--GetDefaults.md) to retrieve the name of the currently selected printer port.  
  
## Syntax  
  
```  
  
CString GetPortName( ) const;  
  
```  
  
## Return Value  
 The name of the currently selected printer port.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::GetDriverName](../vs140/CPrintDialogEx--GetDriverName.md)   
 [CPrintDialogEx::GetDeviceName](../vs140/CPrintDialogEx--GetDeviceName.md)