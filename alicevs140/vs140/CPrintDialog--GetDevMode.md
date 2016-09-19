---
title: "CPrintDialog::GetDevMode"
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
ms.assetid: 09813975-3e56-4b60-b4d3-134a8342c10c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::GetDevMode
Retrieves the `DEVMODE` structure.  
  
## Syntax  
  
```  
  
LPDEVMODE GetDevMode( ) const;  
```  
  
## Return Value  
 The [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) data structure, which contains information about the device initialization and environment of a print driver. You must unlock the memory taken by this structure with the Windows [GlobalUnlock](http://msdn.microsoft.com/library/windows/desktop/aa366595) function, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 Call this function after calling [DoModal](../vs140/CPrintDialog--DoModal.md) or [GetDefaults](../vs140/CPrintDialog--GetDefaults.md) to retrieve information about the printing device.  
  
## Example  
 See the example for [CPrintDialog::PrintCollate](../vs140/CPrintDialog--PrintCollate.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetDeviceCaps](../vs140/CDC--GetDeviceCaps.md)