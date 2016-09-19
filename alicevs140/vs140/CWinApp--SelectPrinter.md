---
title: "CWinApp::SelectPrinter"
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
ms.assetid: 4f1791b9-901c-42e3-aba0-1aa9f991d475
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::SelectPrinter
Call this member function to select a specific printer, and release the printer that was previously selected in the Print Dialog box.  
  
## Syntax  
  
```  
  
      void SelectPrinter(  
   HANDLE hDevNames,  
   HANDLE hDevMode,  
   BOOL bFreeOld = TRUE   
);  
```  
  
#### Parameters  
 `hDevNames`  
 A handle to a [DEVNAMES](../vs140/DEVNAMES-Structure.md) structure that identifies the driver, device, and output port names of a specific printer.  
  
 `hDevMode`  
 A handle to a [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) structure that specifies information about the device initialization and environment of a printer.  
  
 *bFreeOld*  
 Frees the previously-selected printer.  
  
## Remarks  
 If both `hDevMode` and `hDevNames` are **NULL**, `SelectPrinter` uses the current default printer.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565)   
 [DEVNAMES Structure](../vs140/DEVNAMES-Structure.md)