---
title: "CDaoQueryDef::Close"
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
ms.assetid: 6781bedf-f705-416b-80ac-cdc02f48caad
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::Close
Call this member function when you finish using the querydef object.  
  
## Syntax  
  
```  
  
virtual void Close( );  
  
```  
  
## Remarks  
 Closing the querydef releases the underlying DAO object but does not destroy the saved DAO querydef object or the C++ `CDaoQueryDef` object. This is not the same as [CDaoDatabase::DeleteQueryDef](../vs140/CDaoDatabase--DeleteQueryDef.md), which deletes the querydef from the database's QueryDefs collection in DAO (if not a temporary querydef).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::Open](../vs140/CDaoQueryDef--Open.md)   
 [CDaoQueryDef::Create](../vs140/CDaoQueryDef--Create.md)   
 [CDaoQueryDef::CDaoQueryDef](../vs140/CDaoQueryDef--CDaoQueryDef.md)