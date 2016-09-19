---
title: "CPrintDialog::GetDefaults"
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
ms.assetid: 84410502-7b77-4d4e-b8a3-234c624e19e9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::GetDefaults
Retrieves the device defaults of the default printer without displaying a dialog box.  
  
## Syntax  
  
```  
  
BOOL GetDefaults( );  
```  
  
## Return Value  
 Nonzero if the function was successful; otherwise 0.  
  
## Remarks  
 The retrieved values are placed in the `m_pd` structure.  
  
 In some cases, a call to this function will call the [constructor](../vs140/CPrintDialog--CPrintDialog.md) for `CPrintDialog` with `bPrintSetupOnly` set to **FALSE**. In these cases, a printer DC and **hDevNames** and **hDevMode** (two handles located in the `m_pd` data member) are automatically allocated.  
  
 If the constructor for `CPrintDialog` was called with `bPrintSetupOnly` set to **FALSE**, this function will not only return **hDevNames** and **hDevMode** (located in **m_pd.hDevNames** and **m_pd.hDevMode**) to the caller, but will also return a printer DC in **m_pd.hDC**. It is the responsibility of the caller to delete the printer DC and call the Windows [GlobalFree](http://msdn.microsoft.com/library/windows/desktop/aa366579) function on the handles when you are finished with the `CPrintDialog` object.  
  
## Example  
 This code fragment gets the default printer's device context and reports to the user the resolution of the printer in dots per inch. (This attribute of the printer's capabilities is often referred to as DPI.)  
  
 [!CODE [NVC_MFCDocView#107](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#107)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::m_pd](../vs140/CPrintDialog--m_pd.md)   
 [CPrintDialog::GetDeviceName](../vs140/CPrintDialog--GetDeviceName.md)   
 [CPrintDialog::GetDriverName](../vs140/CPrintDialog--GetDriverName.md)   
 [CPrintDialog::GetPortName](../vs140/CPrintDialog--GetPortName.md)