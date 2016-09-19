---
title: "CDC::EndPage"
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
ms.assetid: bf4a85bd-08e9-444f-970b-ded418cdc283
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::EndPage
Informs the device that the application has finished writing to a page.  
  
## Syntax  
  
```  
  
int EndPage( );  
```  
  
## Return Value  
 Greater than or equal to 0 if the function is successful, or a negative value if an error occurred.  
  
## Remarks  
 This member function is typically used to direct the device driver to advance to a new page.  
  
 This member function replaces the **NEWFRAME** printer escape. Unlike **NEWFRAME**, this function is always called after printing a page.  
  
## Example  
 See the example for [CDC::StartDoc](../vs140/CDC--StartDoc.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::StartPage](../vs140/CDC--StartPage.md)   
 [CDC::StartDoc](../vs140/CDC--StartDoc.md)   
 [CDC::Escape](../vs140/CDC--Escape.md)