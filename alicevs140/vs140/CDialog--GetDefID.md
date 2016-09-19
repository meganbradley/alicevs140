---
title: "CDialog::GetDefID"
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
ms.assetid: 2e0dd782-bb16-418f-a647-ee04af76f5e6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::GetDefID
Call the `GetDefID` member function to get the ID of the default pushbutton control for a dialog box.  
  
## Syntax  
  
```  
  
DWORD GetDefID( ) const;  
```  
  
## Return Value  
 A 32-bit value (`DWORD`). If the default pushbutton has an ID value, the high-order word contains **DC_HASDEFID** and the low-order word contains the ID value. If the default pushbutton does not have an ID value, the return value is 0.  
  
## Remarks  
 This is usually an OK button.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::SetDefID](../vs140/CDialog--SetDefID.md)   
 [DM_GETDEFID](http://msdn.microsoft.com/library/windows/desktop/ms645406)