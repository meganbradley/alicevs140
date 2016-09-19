---
title: "CDC::GetGraphicsMode"
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
ms.assetid: cd6aab41-e26a-40f8-982c-6ab403e76610
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetGraphicsMode
Retrieves the current graphics mode for the specified device context.  
  
## Syntax  
  
```  
int GetGraphicsMode() const;  
```  
  
## Return Value  
 Returns the current graphics mode on success. For a list of the values that this method can return, see [GetGraphicsMode](http://msdn.microsoft.com/library/windows/desktop/dd144892).  
  
 Returns 0 on failure.  
  
 To get extended error information, call [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360).  
  
## Remarks  
 This method wraps the Windows GDI function [GetGraphicsMode](http://msdn.microsoft.com/library/windows/desktop/dd144892).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)