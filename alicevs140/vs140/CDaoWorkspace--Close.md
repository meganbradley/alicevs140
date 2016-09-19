---
title: "CDaoWorkspace::Close"
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
ms.assetid: 5dde9776-0282-4615-b9ff-e3f548634a2c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::Close
Call this member function to close the workspace object.  
  
## Syntax  
  
```  
  
virtual void Close( );  
  
```  
  
## Remarks  
 Closing an open workspace object releases the underlying DAO object and, if the workspace is a member of the Workspaces collection, removes it from the collection. Calling **Close** is good programming practice.  
  
> [!CAUTION]
>  Closing a workspace object closes any open databases in the workspace. This results in any recordsets open in the databases being closed as well, and any pending edits or updates are rolled back. For related information, see the [CDaoDatabase::Close](../vs140/CDaoDatabase--Close.md), [CDaoRecordset::Close](../vs140/CDaoRecordset--Close.md), [CDaoTableDef::Close](../vs140/CDaoTableDef--Close.md), and [CDaoQueryDef::Close](../vs140/CDaoQueryDef--Close.md) member functions.  
  
 Workspace objects are not permanent; they only exist while references to them exist. This means that when the database engine session ends, the workspace and its Databases collection do not persist. You must re-create them for the next session by opening your workspace and database(s) again.  
  
 For related information, see the topic "Close Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoWorkspace::Open](../vs140/CDaoWorkspace--Open.md)