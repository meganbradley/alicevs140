---
title: "CManualAccessor::CreateParameterAccessor"
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
ms.assetid: d0a2095b-b37c-4472-accc-45ef365a18c8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CManualAccessor::CreateParameterAccessor
Allocates memory for the parameter bind structures and initializes the parameter data members.  
  
## Syntax  
  
```  
  
      HRESULT CreateParameterAccessor(   
   int nBindEntries,   
   void* pBuffer,   
   DBLENGTH nBufferSize    
) throw( );  
```  
  
#### Parameters  
 `nBindEntries`  
 [in] Number of columns.  
  
 `pBuffer`  
 [in] A pointer to the buffer where the input columns are stored.  
  
 `nBufferSize`  
 [in] The size of the buffer in bytes.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 You must call this function before calling [AddParameterEntry](../vs140/CManualAccessor--AddParameterEntry.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CManualAccessor Class](../vs140/CManualAccessor-Class.md)   
 [CManualAccessor::CreateAccessor](../vs140/CManualAccessor--CreateAccessor.md)   
 [CManualAccessor::AddParameterEntry](../vs140/CManualAccessor--AddParameterEntry.md)