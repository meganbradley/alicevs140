---
title: "CDaoTableDef::GetSourceTableName"
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
ms.assetid: 0b4d4bce-e9ce-41ca-ad3f-fc95813d3666
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::GetSourceTableName
Call this member function to retrieve the name of an attached table in a source database.  
  
## Syntax  
  
```  
  
CString GetSourceTableName( );  
  
```  
  
## Return Value  
 A `CString` object that specifies the source name of an attached table, or an empty string if a native data table.  
  
## Remarks  
 An attached table is a table in another database linked to a Microsoft Jet database. Data for attached tables remains in the external database, where it can be manipulated by other applications.  
  
 For related information, see the topic "SourceTableName Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::GetRecordCount](../vs140/CDaoTableDef--GetRecordCount.md)   
 [CDaoTableDef::SetSourceTableName](../vs140/CDaoTableDef--SetSourceTableName.md)