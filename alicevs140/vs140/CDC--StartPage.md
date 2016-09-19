---
title: "CDC::StartPage"
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
ms.assetid: 0f9a5df5-e225-4955-b016-58633feb7d37
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::StartPage
Call this member function to prepare the printer driver to receive data.  
  
## Syntax  
  
```  
  
int StartPage( );  
```  
  
## Return Value  
 Greater than or equal to 0 if the function is successful, or a negative value if an error occurred.  
  
## Remarks  
 `StartPage` supersedes the **NEWFRAME** and **BANDINFO** escapes.  
  
 For an overview of the sequence of printing calls, see the [StartDoc](../vs140/CDC--StartDoc.md) member function.  
  
 The system disables the `ResetDC` member function between calls to `StartPage` and `EndPage`.  
  
## Example  
 See the example for [CDC::StartDoc](../vs140/CDC--StartDoc.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Escape](../vs140/CDC--Escape.md)   
 [CDC::EndPage](../vs140/CDC--EndPage.md)