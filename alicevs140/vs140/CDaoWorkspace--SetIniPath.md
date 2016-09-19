---
title: "CDaoWorkspace::SetIniPath"
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
ms.assetid: 39f8e4ef-7e46-417a-9d8a-4ab7e7eb1ad5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::SetIniPath
Call this member function to specify the location of Windows registry settings for the Microsoft Jet database engine.  
  
## Syntax  
  
```  
  
      static void PASCAL SetIniPath(   
   LPCTSTR lpszRegistrySubKey    
);  
```  
  
#### Parameters  
 *lpszRegistrySubkey*  
 A string containing the name of a Windows registry subkey for the location of Microsoft Jet database engine settings or parameters needed for installable ISAM databases.  
  
## Remarks  
 Call `SetIniPath` only if you need to specify special settings. For more information, see the topic "IniPath Property" in DAO Help.  
  
> [!NOTE]
>  Call `SetIniPath` during application installation, not when the application runs. `SetIniPath` must be called before you open any workspaces, databases, or recordsets; otherwise, MFC throws an exception.  
  
 You can use this mechanism to configure the database engine with user-provided registry settings. The scope of this attribute is limited to your application and cannot be changed without restarting your application.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)