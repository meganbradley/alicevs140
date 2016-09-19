---
title: "CManualAccessor::AddBindEntry"
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
ms.assetid: 8556dda9-dda1-4f67-96bc-6031e6c6a271
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CManualAccessor::AddBindEntry
Adds a bind entry to the output columns.  
  
## Syntax  
  
```  
  
      void AddBindEntry(  
   DBORDINAL nOrdinal,  
   DBTYPE wType,  
   DBLENGTH nColumnSize,  
   void* pData,  
   void* pLength = NULL,  
   void* pStatus = NULL   
) throw ( );  
```  
  
#### Parameters  
 See [DBBINDING](https://msdn.microsoft.com/en-us/library/ms716845.aspx) in the *OLE DB Programmer's Reference*.  
  
 `nOrdinal`  
 [in] Column number.  
  
 `wType`  
 [in] Data type.  
  
 `nColumnSize`  
 [in] Column size in bytes.  
  
 `pData`  
 [in] A pointer to the column data stored in the buffer.  
  
 `pLength`  
 [in] A pointer to the field length, if required.  
  
 `pStatus`  
 [in] A pointer to the variable to be bound to the column status, if required.  
  
## Remarks  
 To use this function, you must first call [CreateAccessor](../vs140/CManualAccessor--CreateAccessor.md). You cannot add more entries than the number of columns specified in `CreateAccessor`.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CManualAccessor Class](../vs140/CManualAccessor-Class.md)   
 [DBViewer sample](../vs140/Visual-C---Samples.md)