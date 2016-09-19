---
title: "CDaoDatabase::DeleteRelation"
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
ms.assetid: 843044ba-f01d-43d3-9eda-b5efa6102614
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::DeleteRelation
Call this member function to delete an existing relation from the database object's Relations collection.  
  
## Syntax  
  
```  
  
      void DeleteRelation(   
   LPCTSTR lpszName    
);  
```  
  
#### Parameters  
 `lpszName`  
 The name of the relation to delete.  
  
## Remarks  
 Afterwards, the relation no longer exists.  
  
 For related information, see the topic "Delete Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoDatabase::CreateRelation](../vs140/CDaoDatabase--CreateRelation.md)   
 [CDaoTableDef::Create](../vs140/CDaoTableDef--Create.md)   
 [CDaoQueryDef::Create](../vs140/CDaoQueryDef--Create.md)