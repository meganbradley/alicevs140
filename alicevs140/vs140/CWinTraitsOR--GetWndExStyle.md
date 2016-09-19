---
title: "CWinTraitsOR::GetWndExStyle"
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
ms.assetid: c9afc584-593d-4ed3-a62f-8306a92bf2a5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinTraitsOR::GetWndExStyle
Call this function to retrieve a combination (using the logical OR operator) of the extended styles of the `CWinTraits` object and the default styles specified by `t_dwStyle`.  
  
## Syntax  
  
```  
  
      static DWORD GetWndExStyle(  
   DWORD dwExStyle   
);  
```  
  
#### Parameters  
 `dwExStyle`  
 Extended styles used for creation of a window.  
  
## Return Value  
 A combination of extended styles that are passed in `dwExStyle` and default ones specified by `t_dwExStyle`, using the logical OR operator  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWinTraitsOR Class](../vs140/CWinTraitsOR-Class.md)   
 [CWinTraitsOR::GetWndStyle](../vs140/CWinTraitsOR--GetWndStyle.md)