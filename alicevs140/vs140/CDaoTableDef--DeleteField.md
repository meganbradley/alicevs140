---
title: "CDaoTableDef::DeleteField"
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
ms.assetid: 306348ca-b329-4321-adba-f6f2583ec6f4
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::DeleteField
Call this member function to remove a field and make it inaccessible.  
  
## Syntax  
  
```  
  
      void DeleteField(   
   LPCTSTR lpszName    
);  
void DeleteField(   
   int nIndex    
);  
```  
  
#### Parameters  
 `lpszName`  
 A pointer to a string expression that is the name of an existing field.  
  
 `nIndex`  
 The index of the field in the table's zero-based Fields collection, for lookup by index.  
  
## Remarks  
 You can use this member function on a new object that has not been appended to the database or when [CanUpdate](../vs140/CDaoTableDef--CanUpdate.md) returns nonzero.  
  
 For related information, see the topic "Delete Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md)   
 [CDaoTableDef::CreateIndex](../vs140/CDaoTableDef--CreateIndex.md)   
 [CDaoTableDef::DeleteIndex](../vs140/CDaoTableDef--DeleteIndex.md)