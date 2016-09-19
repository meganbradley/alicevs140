---
title: "CPageSetupDialog::GetPortName"
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
ms.assetid: 60444609-8e48-41ca-b44f-578e30ae4b6d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPageSetupDialog::GetPortName
Call this function after calling `DoModal` to retrieve the name of the currently selected printer port.  
  
## Syntax  
  
```  
  
CString GetPortName( ) const;  
  
```  
  
## Return Value  
 The name of the currently selected printer port.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPageSetupDialog Class](../vs140/CPageSetupDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPageSetupDialog::GetDeviceName](../vs140/CPageSetupDialog--GetDeviceName.md)   
 [CPageSetupDialog::GetDriverName](../vs140/CPageSetupDialog--GetDriverName.md)