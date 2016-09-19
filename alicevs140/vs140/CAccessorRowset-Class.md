---
title: "CAccessorRowset Class"
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
ms.assetid: bd4f58ed-cebf-4d43-8985-1e5fcbf06953
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessorRowset Class
Encapsulates a rowset and its associated accessors in a single class.  
  
## Syntax  
  
```  
template <   
   class TAccessor = CNoAccessor,    
   template <typename T> class TRowset = CRowset    
>  
class CAccessorRowset :   
   public TAccessor,    
   public TRowset<TAccessor>  
```  
  
#### Parameters  
 `TAccessor`  
 An accessor class.  
  
 `TRowset`  
 A rowset class.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[Bind](../vs140/CAccessorRowset--Bind.md)|Creates bindings (used when **bBind** is specified as false in [CCommand::Open](../vs140/CCommand--Open.md)).|  
|[CAccessorRowset](../vs140/CAccessorRowset--CAccessorRowset.md)|Constructor.|  
|[Close](../vs140/CAccessorRowset--Close.md)|Closes the rowset and any accessors.|  
|[FreeRecordMemory](../vs140/CAccessorRowset--FreeRecordMemory.md)|Frees any columns in the current record that need to be freed.|  
|[GetColumnInfo](../vs140/CAccessorRowset--GetColumnInfo.md)|Implements [IColumnsInfo::GetColumnInfo](https://msdn.microsoft.com/en-us/library/ms722704.aspx).|  
  
## Remarks  
 Class `TAccessor` manages the accessor. Class *TRowset* manages the rowset.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)