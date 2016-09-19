---
title: "CDaoDatabase::DeleteQueryDef"
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
ms.assetid: a2780bb4-7a8e-4482-ac98-a3ab235048e9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::DeleteQueryDef
Call this member function to delete the specified querydef — saved query — from the `CDaoDatabase` object's QueryDefs collection.  
  
## Syntax  
  
```  
  
      void DeleteQueryDef(   
   LPCTSTR lpszName    
);  
```  
  
#### Parameters  
 `lpszName`  
 The name of the saved query to delete.  
  
## Remarks  
 Afterwards, that query is no longer defined in the database.  
  
 For information about creating querydef objects, see class [CDaoQueryDef](../vs140/CDaoQueryDef-Class.md). A querydef object becomes associated with a particular `CDaoDatabase` object when you construct the `CDaoQueryDef` object, passing it a pointer to the database object.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::Create](../vs140/CDaoQueryDef--Create.md)   
 [CDaoDatabase::CreateRelation](../vs140/CDaoDatabase--CreateRelation.md)   
 [CDaoTableDef::Create](../vs140/CDaoTableDef--Create.md)