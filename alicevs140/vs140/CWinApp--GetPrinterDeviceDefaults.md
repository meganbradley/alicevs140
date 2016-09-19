---
title: "CWinApp::GetPrinterDeviceDefaults"
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
ms.assetid: fac45f81-11e7-4a72-acdf-36837ac026e4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetPrinterDeviceDefaults
Call this member function to prepare a printer device context for printing.  
  
## Syntax  
  
```  
  
      BOOL GetPrinterDeviceDefaults(  
   struct tagPDA* pPrintDlg   
);  
```  
  
#### Parameters  
 *pPrintDlg*  
 A pointer to a [PRINTDLG](http://msdn.microsoft.com/library/windows/desktop/ms646843) structure.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Retrieves the current printer defaults from the Windows .INI file as necessary, or uses the last printer configuration set by the user in Print Setup.  
  
## Example  
 [!CODE [NVC_MFCWindowing#40](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#40)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)