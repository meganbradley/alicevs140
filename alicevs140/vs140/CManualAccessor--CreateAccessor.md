---
title: "CManualAccessor::CreateAccessor"
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
ms.assetid: 594c8d6d-b49a-4818-a9a5-81c8115d4e42
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CManualAccessor::CreateAccessor
Allocates memory for the column bind structures and initializes the column data members.  
  
## Syntax  
  
```  
  
      HRESULT CreateAccessor(   
   int nBindEntries,   
   void* pBuffer,   
   DBLENGTH nBufferSize    
) throw( );  
```  
  
#### Parameters  
 `nBindEntries`  
 [in] Number of columns. This number should match the number of calls to the [CManualAccessor::AddBindEntry](../vs140/CManualAccessor--AddBindEntry.md) function.  
  
 `pBuffer`  
 [in] A pointer to the buffer where the output columns are stored.  
  
 `nBufferSize`  
 [in] The size of the buffer in bytes.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 Call this function before you call the `CManualAccessor::AddBindEntry` function.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CManualAccessor Class](../vs140/CManualAccessor-Class.md)   
 [DBViewer sample](../vs140/Visual-C---Samples.md)