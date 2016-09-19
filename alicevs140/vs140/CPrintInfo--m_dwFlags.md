---
title: "CPrintInfo::m_dwFlags"
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
ms.assetid: 441b3374-b41e-475e-8fe8-2ef54a9402c6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::m_dwFlags
Contains a combination of flags specifying DocObject printing operations.  
  
## Remarks  
 Valid only if data member **m_bDocObject** is **TRUE**.  
  
 The flags can be one or more of the following values:  
  
-   **PRINTFLAG_MAYBOTHERUSER**  
  
-   **PRINTFLAG_PROMPTUSER**  
  
-   **PRINTFLAG_USERMAYCHANGEPRINTER**  
  
-   **PRINTFLAG_RECOMPOSETODEVICE**  
  
-   **PRINTFLAG_DONTACTUALLYPRINT**  
  
-   **PRINTFLAG_FORCEPROPERTIES**  
  
-   **PRINTFLAG_PRINTTOFILE**  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintInfo::m_bDocObject](../vs140/CPrintInfo--m_bDocObject.md)   
 [CPrintInfo::m_nOffsetPage](../vs140/CPrintInfo--m_nOffsetPage.md)