---
title: "ICommandImpl::m_bCancelWhenExecuting"
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
ms.assetid: d7d33e4c-a862-4e6d-a9a1-4400bfe45b88
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandImpl::m_bCancelWhenExecuting
Indicates whether the command can be canceled when executing.  
  
## Syntax  
  
```  
  
unsigned m_bCancelWhenExecuting:1;  
  
```  
  
## Remarks  
 Defaults to **true** (can be canceled).  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [ICommandImpl Class](../vs140/ICommandImpl-Class.md)   
 [ICommandImpl::m_bCancel](../vs140/ICommandImpl--m_bCancel.md)