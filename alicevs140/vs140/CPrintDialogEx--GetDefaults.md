---
title: "CPrintDialogEx::GetDefaults"
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
ms.assetid: 45588565-fb73-4a73-a5a7-cf59ccf786a2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::GetDefaults
Call this function to retrieve the device defaults of the default printer without displaying a dialog box.  
  
## Syntax  
  
```  
  
BOOL GetDefaults( );  
  
```  
  
## Return Value  
 **TRUE** if successful, otherwise **FALSE**.  
  
## Remarks  
 Creates a printer device context (DC) from the [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) and [DEVNAMES](../vs140/DEVNAMES-Structure.md) structures.  
  
 `GetDefaults` does not display the Print property sheet. Instead, it sets the **hDevNames** and **hDevMode** members of [m_pdex](../vs140/CPrintDialogEx--m_pdex.md) to handles to the [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) and [DEVNAMES](../vs140/DEVNAMES-Structure.md) structures that are initialized for the system default printer. Both **hDevNames** and **hDevMode** must be NULL, or `GetDefaults` fails.  
  
 If the **PD_RETURNDC** flag is set, this function will not only return **hDevNames** and **hDevMode** (located in **m_pdex.hDevNames** and **m_pdex.hDevMode**) to the caller, but will also return a printer DC in **m_pdex.hDC**. It is the responsibility of the caller to delete the printer DC and call the Windows [GlobalFree](http://msdn.microsoft.com/library/windows/desktop/aa366579) function on the handles when you are finished with the `CPrintDialogEx` object.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::m_pdex](../vs140/CPrintDialogEx--m_pdex.md)   
 [CPrintDialog::GetDeviceName](../vs140/CPrintDialog--GetDeviceName.md)   
 [CPrintDialog::GetDriverName](../vs140/CPrintDialog--GetDriverName.md)   
 [CPrintDialog::GetPortName](../vs140/CPrintDialog--GetPortName.md)