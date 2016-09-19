---
title: "CDaoTableDef::RefreshLink"
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
ms.assetid: 487912f4-cf57-42bf-a1a1-93afd6463fd3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::RefreshLink
Call this member function to update the connection information for an attached table.  
  
## Syntax  
  
```  
  
void RefreshLink( );  
  
```  
  
## Remarks  
 You change the connection information for an attached table by calling [SetConnect](../vs140/CDaoTableDef--SetConnect.md) on the corresponding `CDaoTableDef` object and then using the `RefreshLink` member function to update the information. When you call `RefreshLink`, the attached table's properties are not changed.  
  
 To force the modified connect information to take effect, all open [CDaoRecordset](../vs140/CDaoRecordset-Class.md) objects based on this tabledef must be closed.  
  
 For related information, see the topic "RefreshLink Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::SetConnect](../vs140/CDaoTableDef--SetConnect.md)