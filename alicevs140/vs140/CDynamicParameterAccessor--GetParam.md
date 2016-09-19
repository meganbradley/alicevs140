---
title: "CDynamicParameterAccessor::GetParam"
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
ms.assetid: 893a6bf8-7b55-4f6d-8a10-a43b13be7f56
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicParameterAccessor::GetParam
Retrieves the nonstring data for a specified parameter from the parameter buffer.  
  
## Syntax  
  
```  
  
      template < class ctype > bool GetParam(   
   DBORDINAL nParam,   
   ctype* pData    
) const throw( );  
template < class ctype > bool GetParam(   
   TCHAR* pParamName,   
   ctype* pData    
) const throw( );  
void* GetParam(   
   DBORDINAL nParam    
) const throw( );  
void* GetParam(   
   TCHAR* pParamName    
) const throw( );  
```  
  
#### Parameters  
 `ctype`  
 A templated parameter that is the data type.  
  
 `nParam`  
 [in] The parameter number (offset from 1). Parameter 0 is reserved for return values. The parameter number is the index of the parameter based on its order in the SQL or stored procedure call. See [SetParam](../vs140/CDynamicParameterAccessor--SetParam.md) for an example.  
  
 `pParamName`  
 [in] The parameter name.  
  
 `pData`  
 [out] The pointer to the memory containing the data retrieved from the buffer.  
  
## Return Value  
 For nontemplated versions, points to the memory containing the data retrieved from the buffer. For templated versions, returns **true** on success or **false** on failure.  
  
 Use `GetParam` to retrieve nonstring parameter data from the buffer. Use [GetParamString](../vs140/CDynamicParameterAccessor--GetParamString.md) to retrieve string parameter data from the buffer.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicParameterAccessor Class](../vs140/CDynamicParameterAccessor-Class.md)