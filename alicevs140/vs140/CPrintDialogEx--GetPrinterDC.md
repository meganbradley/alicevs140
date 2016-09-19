---
title: "CPrintDialogEx::GetPrinterDC"
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
ms.assetid: c073d109-43fc-425b-82e4-cbabe6861847
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::GetPrinterDC
Returns a handle to the printer device context.  
  
## Syntax  
  
```  
  
HDC GetPrinterDC( ) const;  
  
```  
  
## Return Value  
 A handle to the printer device context.  
  
## Remarks  
 You must call the Windows [DeleteDC](http://msdn.microsoft.com/library/windows/desktop/dd183533) function to delete the device context when you are done using it.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::CreatePrinterDC](../vs140/CPrintDialogEx--CreatePrinterDC.md)