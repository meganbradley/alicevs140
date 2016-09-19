---
title: "CPrintDialogEx::CreatePrinterDC"
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
ms.assetid: 3af762e0-9f92-4cf7-a255-d6999be2c2e2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::CreatePrinterDC
Creates a printer device context (DC) from the [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) and [DEVNAMES](../vs140/DEVNAMES-Structure.md) structures.  
  
## Syntax  
  
```  
  
HDC CreatePrinterDC( );  
  
```  
  
## Return Value  
 Handle to the newly created printer device context.  
  
## Remarks  
 The returned DC is also stored in the **hDC** member of [m_pdex](../vs140/CPrintDialogEx--m_pdex.md).  
  
 This DC is assumed to be the current printer DC, and any other previously obtained printer DCs must be deleted. This function can be called, and the resulting DC used, without ever displaying the Print dialog box.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::GetPrinterDC](../vs140/CPrintDialogEx--GetPrinterDC.md)   
 [CPrintDialogEx::GetDevMode](../vs140/CPrintDialogEx--GetDevMode.md)