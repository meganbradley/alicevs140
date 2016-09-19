---
title: "CDaoQueryDef::CDaoQueryDef"
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
ms.assetid: 54597e10-2af6-4b3a-86a3-ad3d85c68554
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::CDaoQueryDef
Constructs a **CDaoQueryDef** object.  
  
## Syntax  
  
```  
  
      CDaoQueryDef(  
   CDaoDatabase* pDatabase   
);  
```  
  
#### Parameters  
 `pDatabase`  
 A pointer to an open [CDaoDatabase](../vs140/CDaoDatabase-Class.md) object.  
  
## Remarks  
 The object can represent an existing querydef stored in the database's QueryDefs collection, a new query to be stored in the collection, or a temporary query, not to be stored. Your next step depends on the type of querydef:  
  
-   If the object represents an existing querydef, call the object's [Open](../vs140/CDaoQueryDef--Open.md) member function to initialize it.  
  
-   If the object represents a new querydef to be saved, call the object's [Create](../vs140/CDaoQueryDef--Create.md) member function. This adds the object to the database's QueryDefs collection. Then call `CDaoQueryDef` member functions to set the object's attributes. Finally, call [Append](../vs140/CDaoQueryDef--Append.md).  
  
-   If the object represents a temporary querydef (not to be saved in the database), call **Create**, passing an empty string for the query's name. After calling **Create**, initialize the querydef by directly setting its attributes. Do not call **Append**.  
  
 To set the attributes of the querydef, you can use the [SetName](../vs140/CDaoQueryDef--SetName.md), [SetSQL](../vs140/CDaoQueryDef--SetSQL.md), [SetConnect](../vs140/CDaoQueryDef--SetConnect.md), [SetODBCTimeout](../vs140/CDaoQueryDef--SetODBCTimeout.md), and [SetReturnsRecords](../vs140/CDaoQueryDef--SetReturnsRecords.md) member functions.  
  
 When you finish with the querydef object, call its [Close](../vs140/CDaoQueryDef--Close.md) member function. If you have a pointer to the querydef, use the **delete** operator to destroy the C++ object.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::GetConnect](../vs140/CDaoQueryDef--GetConnect.md)   
 [CDaoQueryDef::GetDateCreated](../vs140/CDaoQueryDef--GetDateCreated.md)   
 [CDaoQueryDef::GetDateLastUpdated](../vs140/CDaoQueryDef--GetDateLastUpdated.md)   
 [CDaoQueryDef::GetName](../vs140/CDaoQueryDef--GetName.md)   
 [CDaoQueryDef::GetODBCTimeout](../vs140/CDaoQueryDef--GetODBCTimeout.md)   
 [CDaoQueryDef::GetReturnsRecords](../vs140/CDaoQueryDef--GetReturnsRecords.md)   
 [CDaoQueryDef::GetSQL](../vs140/CDaoQueryDef--GetSQL.md)