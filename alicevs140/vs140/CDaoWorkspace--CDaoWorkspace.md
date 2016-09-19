---
title: "CDaoWorkspace::CDaoWorkspace"
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
ms.assetid: a2496947-7cdb-47dc-bcd4-311d497a6352
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::CDaoWorkspace
Constructs a `CDaoWorkspace` object.  
  
## Syntax  
  
```  
  
CDaoWorkspace( );  
  
```  
  
## Remarks  
 After constructing the C++ object, you have two options:  
  
-   Call the object's [Open](../vs140/CDaoWorkspace--Open.md) member function to open the default workspace or to open an existing object in the Workspaces collection.  
  
-   Or call the object's [Create](../vs140/CDaoWorkspace--Create.md) member function to create a new DAO workspace object. This explicitly starts a new workspace session, which you can refer to via the `CDaoWorkspace` object. After calling **Create**, you can call [Append](../vs140/CDaoWorkspace--Append.md) if you want to add the workspace to the database engine's Workspaces collection.  
  
 See the class overview for [CDaoWorkspace](../vs140/CDaoWorkspace-Class.md) for information about when you need to explicitly create a `CDaoWorkspace` object. Usually, you use workspaces created implicitly when you open a [CDaoDatabase](../vs140/CDaoDatabase-Class.md) object without specifying a workspace or when you open a [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object without specifying a database object. MFC DAO objects created in this way use DAO's default workspace, which is created once and reused.  
  
 To release a workspace and its contained objects, call the workspace object's [Close](../vs140/CDaoWorkspace--Close.md) member function.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)