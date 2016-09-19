---
title: "CDynamicParameterAccessor::GetParamIO"
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
ms.assetid: 9c485e39-c67e-4df7-a707-c773019c4d1e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicParameterAccessor::GetParamIO
Determines whether the specified parameter is an input or output parameter.  
  
## Syntax  
  
```  
  
      bool GetParamIO(   
   DBORDINAL nParam,   
   DBPARAMIO * pParamIO    
) const throw( );  
```  
  
#### Parameters  
 `nParam`  
 [in] The parameter number (offset from 1). Parameter 0 is reserved for return values. The parameter number is the index of the parameter based on its order in the SQL or stored procedure call. See [SetParam](../vs140/CDynamicParameterAccessor--SetParam.md) for an example.  
  
 *pParamIO*  
 A pointer to the variable containing the **DBPARAMIO** type (input or output) of the specified parameter. It is defined as follows:  
  
 `typedef DWORD DBPARAMIO;`  
  
 `enum DBPARAMIOENUM`  
  
 `{   DBPARAMIO_NOTPARAM   = 0,`  
  
 `DBPARAMIO_INPUT      = 0x1,`  
  
 `DBPARAMIO_OUTPUT     = 0x2`  
  
 `};`  
  
## Return Value  
 Returns **true** on success or **false** on failure.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicParameterAccessor Class](../vs140/CDynamicParameterAccessor-Class.md)