---
title: "CDaoTableDef::Open"
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
ms.assetid: f322daeb-3354-43bd-9c8d-21bb2674781c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::Open
Call this member function to open a tabledef previously saved in the database's TableDef's collection.  
  
## Syntax  
  
```  
  
      virtual void Open(   
   LPCTSTR lpszName    
);  
```  
  
#### Parameters  
 `lpszName`  
 A pointer to a string that specifies a table name.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::IsOpen](../vs140/CDaoTableDef--IsOpen.md)   
 [CDaoTableDef::Create](../vs140/CDaoTableDef--Create.md)   
 [CDaoTableDef::Close](../vs140/CDaoTableDef--Close.md)