---
title: "CWinTraits::GetWndExStyle"
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
ms.assetid: a1b4bd84-cb1f-41ea-8bda-4d5d6bd18782
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinTraits::GetWndExStyle
Call this function to retrieve the extended styles of the `CWinTraits` object.  
  
## Syntax  
  
```  
  
      static DWORD GetWndExStyle(  
   DWORD dwExStyle   
);  
```  
  
#### Parameters  
 `dwExStyle`  
 Extended styles used for creation of a window. If `dwExStyle` is 0, the template style values (`t_dwExStyle`) are returned. If `dwExStyle` is nonzero, `dwExStyle` is returned.  
  
## Return Value  
 The extended window styles of the object.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWinTraits Class](../vs140/CWinTraits-Class.md)   
 [CWinTraits::GetWndStyle](../vs140/CWinTraits--GetWndStyle.md)