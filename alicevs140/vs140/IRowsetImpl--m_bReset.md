---
title: "IRowsetImpl::m_bReset"
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
ms.assetid: d423f9f3-4d48-4d0c-b152-684c81a0b34e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetImpl::m_bReset
A bit flag used to determine if the cursor position is defined on the rowset.  
  
## Syntax  
  
```  
  
unsigned m_bReset:1;  
  
```  
  
## Remarks  
 If the consumer calls [GetNextRows](../vs140/IRowsetImpl--GetNextRows.md) with a negative `lOffset` or *cRows* and `m_bReset` is true, `GetNextRows` moves to the end of the rowset. If `m_bReset` is false, the consumer receives an error code, in conformance with the OLE DB specification. The `m_bReset` flag gets set to **true** when the rowset is first created and when the consumer calls [IRowsetImpl::RestartPosition](../vs140/IRowsetImpl--RestartPosition.md). It gets set to **false** when you call `GetNextRows`.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetImpl Class](../vs140/IRowsetImpl-Class.md)