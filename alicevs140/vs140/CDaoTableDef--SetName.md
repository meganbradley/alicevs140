---
title: "CDaoTableDef::SetName"
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
ms.assetid: 261a27c9-a27a-4415-ae6e-61ce479cc5cb
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::SetName
Call this member function to set a user-defined name for a table.  
  
## Syntax  
  
```  
  
      void SetName(   
   LPCTSTR lpszName    
);  
```  
  
#### Parameters  
 `lpszName`  
 A pointer to a string expression that specifies a name for a table.  
  
## Remarks  
 The name must start with a letter and can contain a maximum of 64 characters. It can include numbers and underscore characters but cannot include punctuation or spaces.  
  
 For related information, see the topic "Name Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::RefreshLink](../vs140/CDaoTableDef--RefreshLink.md)   
 [CDaoTableDef::SetConnect](../vs140/CDaoTableDef--SetConnect.md)