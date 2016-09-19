---
title: "CRowsetImpl::NameFromDBID"
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
ms.assetid: 6aa5b074-90c7-4434-adfd-c64c13e76c78
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowsetImpl::NameFromDBID
Extracts a string from a **DBID** and copies it to the `bstr` passed in.  
  
## Syntax  
  
```  
  
      HRESULT CRowsetBaseImpl::NameFromDBID(  
   DBID* pDBID,  
   CComBSTR& bstr,  
   bool bIndex   
);  
```  
  
#### Parameters  
 *pDBID*  
 [in] A pointer to the **DBID** from which to extract a string.  
  
 `bstr`  
 [in] A [CComBSTR](../vs140/CComBSTR-Class.md) reference to place a copy of the **DBID** string.  
  
 `bIndex`  
 [in] **true** if an index **DBID**; **false** if a table **DBID**.  
  
## Return Value  
 A standard `HRESULT`. Depending on whether the **DBID** is a table or an index (denoted by `bIndex`), the method will either return **DB_E_NOINDEX** or **DB_E_NOTABLE**.  
  
## Remarks  
 This method is called by the `CRowsetImpl` implementations of [ValidateCommandID](../vs140/CRowsetImpl--ValidateCommandID.md) and [GetCommandFromID](../vs140/CRowsetImpl--GetCommandFromID.md).  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [CRowsetImpl Class](../vs140/CRowsetImpl-Class.md)