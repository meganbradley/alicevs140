---
title: "CDaoDatabase::DeleteTableDef"
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
ms.assetid: 8c31c889-923a-4585-b7ff-ecc5edf4e7ce
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::DeleteTableDef
Call this member function to delete the specified table and all of its data from the `CDaoDatabase` object's TableDefs collection.  
  
## Syntax  
  
```  
  
      void DeleteTableDef(   
   LPCTSTR lpszName    
);  
```  
  
#### Parameters  
 `lpszName`  
 The name of the tabledef to delete.  
  
## Remarks  
 Afterwards, that table is no longer defined in the database.  
  
> [!NOTE]
>  Be very careful not to delete system tables.  
  
 For information about creating tabledef objects, see class [CDaoTableDef](../vs140/CDaoTableDef-Class.md). A tabledef object becomes associated with a particular `CDaoDatabase` object when you construct the `CDaoTableDef` object, passing it a pointer to the database object.  
  
 For related information, see the topic "Delete Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::Create](../vs140/CDaoTableDef--Create.md)   
 [CDaoQueryDef::Create](../vs140/CDaoQueryDef--Create.md)   
 [CDaoDatabase::CreateRelation](../vs140/CDaoDatabase--CreateRelation.md)