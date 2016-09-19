---
title: "CPrintDialog::GetDeviceName"
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
ms.assetid: 0e544b79-1502-4c1e-803a-fc9b13fe2908
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::GetDeviceName
Retrieves the name of the currently selected printer device.  
  
## Syntax  
  
```  
  
CString GetDeviceName( ) const;  
```  
  
## Return Value  
 The name of the currently selected printer.  
  
## Remarks  
 Call this function after calling [DoModal](../vs140/CPrintDialog--DoModal.md) to retrieve the name of the currently selected printer, or after calling [GetDefaults](../vs140/CPrintDialog--GetDefaults.md) to retrieve the current device defaults of the default printer. Use a pointer to the `CString` object returned by `GetDeviceName` as the value of `lpszDeviceName` in a call to [CDC::CreateDC](../vs140/CDC--CreateDC.md).  
  
## Example  
 This code fragment shows the user's default printer name and the port it is connected to, along with the spooler name the printer uses. The code might show a message box that says, "Your default printer is HP LaserJet IIIP on \\\server\share using winspool.", for example.  
  
 [!CODE [NVC_MFCDocView#108](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#108)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::GetDriverName](../vs140/CPrintDialog--GetDriverName.md)   
 [CPrintDialog::GetDevMode](../vs140/CPrintDialog--GetDevMode.md)   
 [CPrintDialog::GetPortName](../vs140/CPrintDialog--GetPortName.md)