---
title: "ICommandUI::ContinueRouting"
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
ms.assetid: 71b59aa5-6c96-4eef-ba85-7f31da1bff1f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandUI::ContinueRouting
Tells the command routing mechanism to continue routing the current message down the chain of handlers.  
  
## Syntax  
  
```  
void ContinueRouting( );  
```  
  
## Remarks  
 This is an advanced member function that should be used in conjunction with an [ON_COMMAND_EX](../vs140/ON_COMMAND_EX.md) handler that returns `FALSE`. For more information, see Technical Note [TN006: Message Maps](../vs140/TN006--Message-Maps.md).  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [ICommandUI Interface](../vs140/ICommandUI-Interface.md)   
 [ON_COMMAND_EX](../vs140/ON_COMMAND_EX.md)