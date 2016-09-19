---
title: "CWinTraits::GetWndStyle"
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
ms.assetid: e82b22b0-9e2e-41ac-bc16-fb2a24b7973d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinTraits::GetWndStyle
Call this function to retrieve the standard styles of the `CWinTraits` object.  
  
## Syntax  
  
```  
  
      static DWORD GetWndStyle(  
   DWORD dwStyle   
);  
```  
  
#### Parameters  
 `dwStyle`  
 Standard styles used for creation of a window. If `dwStyle` is 0, the template style values (`t_dwStyle`) are returned. If `dwStyle` is nonzero, `dwStyle` is returned.  
  
## Return Value  
 The standard window styles of the object.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWinTraits Class](../vs140/CWinTraits-Class.md)   
 [CWinTraits::GetWndExStyle](../vs140/CWinTraits--GetWndExStyle.md)