---
title: "ICommandImpl::m_bIsExecuting"
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
ms.assetid: 1e152164-514c-4116-88a3-16984af99991
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandImpl::m_bIsExecuting
Indicates whether the command is currently executing.  
  
## Syntax  
  
```  
  
unsigned m_bIsExecuting:1;  
  
```  
  
## Remarks  
 The **Execute** method of your command class can set this variable to **true**.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [ICommandImpl Class](../vs140/ICommandImpl-Class.md)   
 [ICommandImpl::m_bCancelWhenExecuting](../vs140/ICommandImpl--m_bCancelWhenExecuting.md)