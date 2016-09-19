---
title: "CWinTraitsOR::GetWndStyle"
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
ms.assetid: d81cbf6f-d21d-4432-8b3f-83aa27995c03
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinTraitsOR::GetWndStyle
Call this function to retrieve a combination (using the logical OR operator) of the standard styles of the `CWinTraits` object and the default styles specified by `t_dwStyle`.  
  
## Syntax  
  
```  
  
      static DWORD GetWndStyle(  
   DWORD dwStyle   
);  
```  
  
#### Parameters  
 `dwStyle`  
 Styles used for creation of a window.  
  
## Return Value  
 A combination of styles that are passed in `dwStyle` and the default ones specified by `t_dwStyle`, using the logical OR operator.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWinTraitsOR Class](../vs140/CWinTraitsOR-Class.md)   
 [CWinTraitsOR::GetWndExStyle](../vs140/CWinTraitsOR--GetWndExStyle.md)