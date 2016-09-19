---
title: "ICommandImpl::m_bCancel"
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
ms.assetid: f3b6fb60-4de4-4d81-a5d2-4052c41be0de
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandImpl::m_bCancel
Indicates whether the command is canceled.  
  
## Syntax  
  
```  
  
unsigned m_bCancel:1;  
  
```  
  
## Remarks  
 You can retrieve this variable in the **Execute** method of your command class and cancel as appropriate.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [ICommandImpl Class](../vs140/ICommandImpl-Class.md)   
 [ICommandImpl::m_bCancelWhenExecuting](../vs140/ICommandImpl--m_bCancelWhenExecuting.md)