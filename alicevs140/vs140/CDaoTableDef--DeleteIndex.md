---
title: "CDaoTableDef::DeleteIndex"
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
ms.topic: reference
ms.assetid: a3c5693d-0dbf-46ed-8422-927c6946cfeb
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::DeleteIndex
Call this member function to delete an index in an underlying table.  
  
## Syntax  
  
```  
  
      void DeleteIndex(   
   LPCTSTR lpszName    
);  
void DeleteIndex(   
   int nIndex    
);  
```  
  
#### Parameters  
 `lpszName`  
 A pointer to a string expression that is the name of an existing index.  
  
 `nIndex`  
 The array index of the index object in the database's zero-based TableDefs collection, for lookup by index.  
  
## Remarks  
 You can use this member function on a new object that hasn't been appended to the database or when [CanUpdate](../vs140/CDaoTableDef--CanUpdate.md) returns nonzero.  
  
 For related information, see the topic "Delete Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::CreateIndex](../vs140/CDaoTableDef--CreateIndex.md)   
 [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md)   
 [CDaoTableDef::DeleteField](../vs140/CDaoTableDef--DeleteField.md)