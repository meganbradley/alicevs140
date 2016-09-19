---
title: "CDaoWorkspace::Open"
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
ms.assetid: 30bbd102-0d6e-411b-ab97-3377d3379a6f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::Open
Explicitly opens a workspace object associated with DAO's default workspace.  
  
## Syntax  
  
```  
  
      virtual void Open(   
   LPCTSTR lpszName = NULL    
);  
```  
  
#### Parameters  
 `lpszName`  
 The name of the DAO workspace object to open — a string with up to 14 characters that uniquely names the workspace. Accept the default value **NULL** to explicitly open the default workspace. For naming requirements, see the `lpszName` parameter for [Create](../vs140/CDaoWorkspace--Create.md). For related information, see the topic "Name Property" in DAO Help.  
  
## Remarks  
 After constructing a `CDaoWorkspace` object, call this member function to do one of the following:  
  
-   Explicitly open the default workspace. Pass **NULL** for `lpszName`.  
  
-   Open an existing `CDaoWorkspace` object, a member of the Workspaces collection, by name. Pass a valid name for an existing workspace object.  
  
 **Open** puts the workspace object into an open state and also initializes the database engine if it has not already been initialized for your application.  
  
 Although many `CDaoWorkspace` member functions can only be called after the workspace has been opened, the following member functions, which operate on the database engine, are available after construction of the C++ object but before a call to **Open**:  
  
||||  
|-|-|-|  
|[Create](../vs140/CDaoWorkspace--Create.md)|[GetVersion](../vs140/CDaoWorkspace--GetVersion.md)|[SetDefaultUser](../vs140/CDaoWorkspace--SetDefaultUser.md)|  
|[GetIniPath](../vs140/CDaoWorkspace--GetIniPath.md)|[Idle](../vs140/CDaoWorkspace--Idle.md)|[SetIniPath](../vs140/CDaoWorkspace--SetIniPath.md)|  
|[GetLoginTimeout](../vs140/CDaoWorkspace--GetLoginTimeout.md)|[SetDefaultPassword](../vs140/CDaoWorkspace--SetDefaultPassword.md)|[SetLoginTimeout](../vs140/CDaoWorkspace--SetLoginTimeout.md)|  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoWorkspace::IsOpen](../vs140/CDaoWorkspace--IsOpen.md)   
 [CDaoWorkspace::CDaoWorkspace](../vs140/CDaoWorkspace--CDaoWorkspace.md)   
 [CDaoWorkspace::Create](../vs140/CDaoWorkspace--Create.md)   
 [CDaoWorkspace::Close](../vs140/CDaoWorkspace--Close.md)