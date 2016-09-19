---
title: "CDaoWorkspace::Create"
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
ms.assetid: 696cd4ae-7aa7-421d-995b-07aac1e17179
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::Create
Call this member function to create a new DAO workspace object and associate it with the MFC `CDaoWorkspace` object.  
  
## Syntax  
  
```  
  
      virtual void Create(   
   LPCTSTR lpszName,   
   LPCTSTR lpszUserName,   
   LPCTSTR lpszPassword    
);  
```  
  
#### Parameters  
 `lpszName`  
 A string with up to 14 characters that uniquely names the new workspace object. You must supply a name. For related information, see the topic "Name Property" in DAO Help.  
  
 *lpszUserName*  
 The user name of the workspace's owner. For requirements, see the `lpszDefaultUser` parameter to the [SetDefaultUser](../vs140/CDaoWorkspace--SetDefaultUser.md) member function. For related information, see the topic "UserName Property" in DAO Help.  
  
 `lpszPassword`  
 The password for the new workspace object. A password can be up to 14 characters long and can contain any character except ASCII 0 (null). Passwords are case-sensitive. For related information, see the topic "Password Property" in DAO Help.  
  
## Remarks  
 The overall creation process is:  
  
1.  Construct a [CDaoWorkspace](../vs140/CDaoWorkspace--CDaoWorkspace.md) object.  
  
2.  Call the object's **Create** member function to create the underlying DAO workspace. You must specify a workspace name.  
  
3.  Optionally call [Append](../vs140/CDaoWorkspace--Append.md) if you want to add the workspace to the database engine's Workspaces collection. You can work with the workspace without appending it.  
  
 After the **Create** call, the workspace object is in an open state, ready for use. You do not call **Open** after **Create**. You do not call **Create** if the workspace already exists in the Workspaces collection. **Create** initializes the database engine if it has not already been initialized for your application.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoWorkspace::CDaoWorkspace](../vs140/CDaoWorkspace--CDaoWorkspace.md)   
 [CDaoWorkspace::Close](../vs140/CDaoWorkspace--Close.md)   
 [CDaoWorkspace::Open](../vs140/CDaoWorkspace--Open.md)