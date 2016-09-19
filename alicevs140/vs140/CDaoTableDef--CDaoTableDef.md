---
title: "CDaoTableDef::CDaoTableDef"
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
ms.assetid: f90a5918-0bd5-4ea6-83de-cc0f0055fd59
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::CDaoTableDef
Constructs a **CDaoTableDef** object.  
  
## Syntax  
  
```  
  
      CDaoTableDef(  
   CDaoDatabase* pDatabase   
);  
```  
  
#### Parameters  
 `pDatabase`  
 A pointer to a [CDaoDatabase](../vs140/CDaoDatabase-Class.md) object.  
  
## Remarks  
 After constructing the object, you must call the [Create](../vs140/CDaoTableDef--Create.md) or [Open](../vs140/CDaoTableDef--Open.md) member function. When you finish with the object, you must call its [Close](../vs140/CDaoTableDef--Close.md) member function and destroy the `CDaoTableDef` object.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::Open](../vs140/CDaoTableDef--Open.md)   
 [CDaoTableDef::Close](../vs140/CDaoTableDef--Close.md)   
 [CDaoTableDef::Create](../vs140/CDaoTableDef--Create.md)   
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)