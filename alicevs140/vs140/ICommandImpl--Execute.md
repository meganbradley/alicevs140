---
title: "ICommandImpl::Execute"
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
ms.assetid: 033e0d4e-256b-4eed-9215-70e0bebb768c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandImpl::Execute
Executes the command.  
  
## Syntax  
  
```  
  
      HRESULT Execute(  
   IUnknown* pUnkOuter,  
   REFIID riid,  
   DBPARAMS* pParams,  
   DBROWCOUNT* pcRowsAffected,  
   IUnknown** ppRowset   
);  
```  
  
#### Parameters  
 See [ICommand::Execute](https://msdn.microsoft.com/en-us/library/ms718095.aspx) in the *OLE DB Programmer's Reference*.  
  
## Remarks  
 The outgoing interface requested will be an interface acquired from the rowset object that this function creates.  
  
 **Execute** calls [CreateRowset](../vs140/ICommandImpl--CreateRowset.md). Override the default implementation to create more than one rowset or to provide your own conditions for creating different rowsets.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [ICommandImpl Class](../vs140/ICommandImpl-Class.md)   
 [ICommandImpl::CancelExecution](../vs140/ICommandImpl--CancelExecution.md)