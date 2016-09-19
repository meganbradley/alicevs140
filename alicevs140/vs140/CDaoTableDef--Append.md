---
title: "CDaoTableDef::Append"
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
ms.assetid: b5e705c1-bb06-48a5-93e4-72a536bb17c6
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::Append
Call this member function after you call [Create](../vs140/CDaoTableDef--Create.md) to create a new tabledef object to save the tabledef in the database.  
  
## Syntax  
  
```  
  
virtual void Append( );  
  
```  
  
## Remarks  
 The function appends the object to the database's TableDefs collection. You can use the tabledef as a temporary object while defining it by not appending it, but if you want to save and use it, you must call **Append**.  
  
> [!NOTE]
>  If you attempt to append an unnamed tabledef (containing a null or empty string), MFC throws an exception.  
  
 For related information, see the topic "Append Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::Create](../vs140/CDaoTableDef--Create.md)