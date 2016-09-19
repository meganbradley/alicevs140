---
title: "CPageSetupDialog::GetDevMode"
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
ms.assetid: 9fcd3f05-0fe8-4631-96e3-0b49f67472d6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPageSetupDialog::GetDevMode
Call this function after calling `DoModal` to retrieve information about the printer device context of the `CPageSetupDialog` object.  
  
## Syntax  
  
```  
  
LPDEVMODE GetDevMode( ) const;  
  
```  
  
## Return Value  
 The [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) data structure, which contains information about the device initialization and environment of a print driver. You must unlock the memory taken by this structure with the Windows [GlobalUnlock](http://msdn.microsoft.com/library/windows/desktop/aa366595) function, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPageSetupDialog Class](../vs140/CPageSetupDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)