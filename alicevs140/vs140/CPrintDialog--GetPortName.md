---
title: "CPrintDialog::GetPortName"
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
ms.assetid: 7decf747-4e87-47b3-ba6b-7a4d3053540d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::GetPortName
Retrieves the name of the currently selected printer port.  
  
## Syntax  
  
```  
  
CString GetPortName( ) const;  
```  
  
## Return Value  
 The name of the currently selected printer port.  
  
## Remarks  
 Call this function after calling [DoModal](../vs140/CPrintDialog--DoModal.md) or [GetDefaults](../vs140/CPrintDialog--GetDefaults.md) to retrieve the name of the currently selected printer port.  
  
## Example  
 See the example for [CPrintDialog::GetDeviceName](../vs140/CPrintDialog--GetDeviceName.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::GetDriverName](../vs140/CPrintDialog--GetDriverName.md)   
 [CPrintDialog::GetDeviceName](../vs140/CPrintDialog--GetDeviceName.md)