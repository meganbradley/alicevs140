---
title: "CCommand::Prepare"
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
ms.assetid: f0e473fc-2f7a-4d29-96c2-1328dc21e702
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommand::Prepare
Validates and optimizes the current command.  
  
## Syntax  
  
```  
  
      HRESULT CCommandBase::Prepare(  
   ULONG cExpectedRuns = 0   
) throw( );  
```  
  
#### Parameters  
 *cExpectedRuns*  
 [in] The number of times you expect to execute the command.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 This method wraps the OLE DB method [ICommandPrepare::Prepare](https://msdn.microsoft.com/en-us/library/ms718370.aspx).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CCommand Class](../vs140/CCommand-Class.md)