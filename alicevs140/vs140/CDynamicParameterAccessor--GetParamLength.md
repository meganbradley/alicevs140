---
title: "CDynamicParameterAccessor::GetParamLength"
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
ms.assetid: 04d76931-911a-4915-9c2c-ad585a9f3854
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicParameterAccessor::GetParamLength
Retrieves the length of the specified parameter stored in the buffer.  
  
## Syntax  
  
```  
  
      bool GetParamLength(  
   DBORDINAL nParam,  
   DBLENGTH* pLength  
);  
DBLENGTH* GetParamLength(   
   DBORDINAL nParam    
) const throw( );  
```  
  
#### Parameters  
 `nParam`  
 [in] The parameter number (offset from 1). Parameter 0 is reserved for return values. The parameter number is the index of the parameter based on its order in the SQL or stored procedure call. See [SetParam](../vs140/CDynamicParameterAccessor--SetParam.md) for an example.  
  
 `pLength`  
 [out] A pointer to the variable containing the length in bytes of the specified parameter.  
  
## Remarks  
 The first override returns **true** on success or **false** on failure. The second override points to the memory containing the length of the parameter.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicParameterAccessor Class](../vs140/CDynamicParameterAccessor-Class.md)