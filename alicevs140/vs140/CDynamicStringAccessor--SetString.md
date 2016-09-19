---
title: "CDynamicStringAccessor::SetString"
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
ms.assetid: 94846d8b-4c1b-47fe-acdc-1752981cee25
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicStringAccessor::SetString
Sets the specified column data as a string.  
  
## Syntax  
  
```  
HRESULT SetString(  
   DBORDINAL nColumn,  
   BaseType* data  
) throw( );  
HRESULT SetString(  
   const CHAR* pColumnName,  
   BaseType* data  
) throw( );  
HRESULT SetString(  
   const WCHAR* pColumnName,  
   BaseType* data  
) throw( );  
```  
  
#### Parameters  
 `nColumn`  
 [in] The column number. Column numbers start with 1. The special value of 0 refers to the bookmark column, if any.  
  
 `pColumnName`  
 [in] A pointer to a character string that contains the column name.  
  
 `data`  
 [in] A pointer to the string data to be written to the specified column.  
  
## Return Value  
 A pointer to the string value to which to set the specified column. The value is of type `BaseType`, which will be `CHAR` or `WCHAR` depending on whether `_UNICODE` is defined or not.  
  
## Remarks  
 The second override form takes the column name as an ANSI string and the third override form takes the column name as a Unicode string.  
  
 If `_SECURE_ATL` is defined to have a nonzero value, a runtime assertion failure will be generated if the input `data` string is longer than the maximum allowable length of the referenced data column. Otherwise, the input string will be truncated if it is longer than the maximum allowable length.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDynamicStringAccessor Class](../vs140/CDynamicStringAccessor-Class.md)