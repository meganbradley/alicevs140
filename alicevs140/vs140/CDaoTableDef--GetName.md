---
title: "CDaoTableDef::GetName"
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
ms.assetid: 3625f6aa-cea6-4b15-9ef3-9174ac6588f5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::GetName
Call this member function to obtain the user-defined name of the underlying table.  
  
## Syntax  
  
```  
  
CString GetName( );  
  
```  
  
## Return Value  
 A user-defined name for a table.  
  
## Remarks  
 This name starts with a letter and can contain a maximum of 64 characters. It can include numbers and underscore characters but cannot include punctuation or spaces.  
  
 For related information, see the topic "Name Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::SetName](../vs140/CDaoTableDef--SetName.md)   
 [CDaoTableDef::GetConnect](../vs140/CDaoTableDef--GetConnect.md)   
 [CDaoTableDef::SetConnect](../vs140/CDaoTableDef--SetConnect.md)