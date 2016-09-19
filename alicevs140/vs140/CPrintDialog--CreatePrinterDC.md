---
title: "CPrintDialog::CreatePrinterDC"
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
ms.assetid: 2e80c2e8-7b5f-4b39-ac31-5249fa574b57
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::CreatePrinterDC
Creates a printer device context (DC) from the [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) and [DEVNAMES](../vs140/DEVNAMES-Structure.md) structures.  
  
## Syntax  
  
```  
  
HDC CreatePrinterDC( );  
```  
  
## Return Value  
 Handle to the newly created printer device context.  
  
## Remarks  
 This DC is assumed to be the current printer DC, and any other previously obtained printer DCs must be deleted by the user. This function can be called, and the resulting DC used, without ever displaying the Print dialog box.  
  
## Example  
 [!CODE [NVC_MFCDocView#106](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#106)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::GetDevMode](../vs140/CPrintDialog--GetDevMode.md)