---
title: "CDC::DrawEscape"
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
ms.assetid: 8107c2d4-226f-4a2f-8d63-94ed376608de
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::DrawEscape
Accesses drawing capabilities of a video display that are not directly available through the graphics device interface (GDI).  
  
## Syntax  
  
```  
  
      int DrawEscape(  
   int nEscape,  
   int nInputSize,  
   LPCSTR lpszInputData   
);  
```  
  
#### Parameters  
 `nEscape`  
 Specifies the escape function to be performed.  
  
 `nInputSize`  
 Specifies the number of bytes of data pointed to by the `lpszInputData` parameter.  
  
 `lpszInputData`  
 Points to the input structure required for the specified escape.  
  
## Return Value  
 Specifies the outcome of the function. Greater than zero if successful, except for the **QUERYESCSUPPORT** draw escape, which checks for implementation only; or zero if the escape is not implemented; or less than zero if an error occurred.  
  
## Remarks  
 When an application calls `DrawEscape`, the data identified by `nInputSize` and `lpszInputData` is passed directly to the specified display driver.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Escape](../vs140/CDC--Escape.md)   
 [DrawEscape](http://msdn.microsoft.com/library/windows/desktop/dd162478)