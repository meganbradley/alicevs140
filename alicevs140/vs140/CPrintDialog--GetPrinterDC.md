---
title: "CPrintDialog::GetPrinterDC"
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
ms.assetid: b5598cad-bae0-4b23-a054-2516d0a7e3c2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::GetPrinterDC
Retrieves a handle to the printer device context.  
  
## Syntax  
  
```  
  
HDC GetPrinterDC( ) const;  
```  
  
## Return Value  
 A handle to the printer device context if successful; otherwise **NULL**.  
  
## Remarks  
 If the `bPrintSetupOnly` parameter of the `CPrintDialog` constructor was **FALSE** (indicating that the Print dialog box is displayed), then `GetPrinterDC` returns a handle to the printer device context. You must call the Windows [DeleteDC](http://msdn.microsoft.com/library/windows/desktop/dd183533) function to delete the device context when you are done using it.  
  
## Example  
 [!CODE [NVC_MFCDocView#109](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#109)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)