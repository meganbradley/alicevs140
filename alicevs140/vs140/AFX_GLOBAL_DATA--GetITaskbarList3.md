---
title: "AFX_GLOBAL_DATA::GetITaskbarList3"
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
ms.topic: article
ms.assetid: 5266f980-7e30-4657-bb67-1ae0aeab3e27
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_GLOBAL_DATA::GetITaskbarList3
Creates and stores in the global data a pointer to the `ITaskBarList3` interface.  
  
## Syntax  
  
```  
ITaskbarList3 *GetITaskbarList3();  
```  
  
## Return Value  
 A pointer to the `ITaskbarList3` interface if creation of a task bar list object succeeds; `NULL` if creation fails or if the current Operation System is less than Windows 7.  
  
## Remarks  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)