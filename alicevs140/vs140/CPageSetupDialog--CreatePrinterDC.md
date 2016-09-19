---
title: "CPageSetupDialog::CreatePrinterDC"
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
ms.assetid: 50097a9d-f7ee-4017-af9c-146e5382d57c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPageSetupDialog::CreatePrinterDC
Creates a printer device context from the [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) and [DEVNAMES](../vs140/DEVNAMES-Structure.md) structures.  
  
## Syntax  
  
```  
  
HDC CreatePrinterDC( );  
  
```  
  
## Return Value  
 Handle to the newly created printer device context (DC).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPageSetupDialog Class](../vs140/CPageSetupDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPageSetupDialog::GetDevMode](../vs140/CPageSetupDialog--GetDevMode.md)   
 [CPageSetupDialog::GetDeviceName](../vs140/CPageSetupDialog--GetDeviceName.md)   
 [CPageSetupDialog::GetDriverName](../vs140/CPageSetupDialog--GetDriverName.md)