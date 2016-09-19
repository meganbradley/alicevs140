---
title: "ICommandImpl Class"
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
ms.assetid: ef285fef-0d66-45e6-a762-b03357098e3b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandImpl Class
Provides implementation for the [ICommand](https://msdn.microsoft.com/en-us/library/ms709737.aspx) interface.  
  
## Syntax  
  
```  
template <class T, class CommandBase = ICommand>   
class ATL_NO_VTABLE ICommandImpl : public CommandBase  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `ICommandImpl`.  
  
 `CommandBase`  
 A command interface. The default is `ICommand`.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[CancelExecution](../vs140/ICommandImpl--CancelExecution.md)|Cancels the current command execution.|  
|[Cancel](../vs140/ICommandImpl--Cancel.md)|Cancels the current command execution.|  
|[CreateRowset](../vs140/ICommandImpl--CreateRowset.md)|Creates a rowset object.|  
|[Execute](../vs140/ICommandImpl--Execute.md)|Executes the command.|  
|[GetDBSession](../vs140/ICommandImpl--GetDBSession.md)|Returns an interface pointer to the session that created the command.|  
|[ICommandImpl](../vs140/ICommandImpl--ICommandImpl.md)|The constructor.|  
  
### Data Members  
  
|||  
|-|-|  
|[m_bCancel](../vs140/ICommandImpl--m_bCancel.md)|Indicates whether the command is to be canceled.|  
|[m_bCancelWhenExecuting](../vs140/ICommandImpl--m_bCancelWhenExecuting.md)|Indicates whether the command is to be canceled when executing.|  
|[m_bIsExecuting](../vs140/ICommandImpl--m_bIsExecuting.md)|Indicates whether the command is currently executing.|  
  
## Remarks  
 A mandatory interface on the command object.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)