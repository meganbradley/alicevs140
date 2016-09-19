---
title: "CDynamicParameterAccessor::GetParamString"
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
ms.assetid: 078c2b1c-7072-47c1-a203-f47e75363f91
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicParameterAccessor::GetParamString
Retrieves the string data of the specified parameter stored in the buffer.  
  
## Syntax  
  
```  
  
      bool GetParamString(  
   DBORDINAL nParam,  
   CSimpleStringA& strOutput  
) throw( );  
bool GetParamString(  
   DBORDINAL nParam,  
   CSimpleStringW& strOutput  
) throw( );  
bool GetParamString(  
   DBORDINAL nParam,  
   CHAR* pBuffer,  
   size_t* pMaxLen  
) throw( );  
bool GetParamString(  
   DBORDINAL nParam,  
   WCHAR* pBuffer,  
   size_t* pMaxLen  
) throw( );  
```  
  
#### Parameters  
 `nParam`  
 [in] The parameter number (offset from 1). Parameter 0 is reserved for return values. The parameter number is the index of the parameter based on its order in the SQL or stored procedure call. See [SetParam](../vs140/CDynamicParameterAccessor--SetParam.md) for an example.  
  
 `strOutput`  
 [out] The ANSI (**CSimpleStringA**) or Unicode (**CSimpleStringW**) string data of the specified parameter. You should pass a parameter of type `CString`, for example:  
  
 [!CODE [NVC_OLEDB_Consumer#9](../CodeSnippet/VS_Snippets_Cpp/NVC_OLEDB_Consumer#9)]  
  
 `pBuffer`  
 [out] A pointer to the ANSI (**CHAR**) or Unicode (**WCHAR**) string data of the specified parameter.  
  
 `pMaxLen`  
 [out] A pointer to the size of the buffer pointed to by `pBuffer` (in characters, including the terminating NULL).  
  
## Remarks  
 Returns **true** on success or **false** on failure.  
  
 If `pBuffer` is NULL, this method will set the required buffer size in the memory pointed to by `pMaxLen` and return **true** without copying the data.  
  
 This method will fail if the buffer `pBuffer` is not large enough to contain the whole string.  
  
 Use `GetParamString` to retrieve string parameter data from the buffer. Use [GetParam](../vs140/CDynamicParameterAccessor--GetParam.md) to retrieve nonstring parameter data from the buffer.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicParameterAccessor Class](../vs140/CDynamicParameterAccessor-Class.md)