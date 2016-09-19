---
title: "CDaoQueryDef::SetName"
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
ms.assetid: 60cda5c0-0b47-467b-8b0a-95becd79d243
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::SetName
Call this member function if you want to change the name of a querydef that is not temporary.  
  
## Syntax  
  
```  
  
      void SetName(   
   LPCTSTR lpszName    
);  
```  
  
#### Parameters  
 `lpszName`  
 A string that contains the new name for a nontemporary query in the associated [CDaoDatabase](../vs140/CDaoDatabase-Class.md) object.  
  
## Remarks  
 Querydef names are unique, user-defined names. You can call `SetName` before the querydef object is appended to the QueryDefs collection.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::GetName](../vs140/CDaoQueryDef--GetName.md)   
 [CDaoQueryDef::SetSQL](../vs140/CDaoQueryDef--SetSQL.md)   
 [CDaoQueryDef::SetConnect](../vs140/CDaoQueryDef--SetConnect.md)   
 [CDaoQueryDef::SetODBCTimeout](../vs140/CDaoQueryDef--SetODBCTimeout.md)   
 [CDaoQueryDef::SetReturnsRecords](../vs140/CDaoQueryDef--SetReturnsRecords.md)