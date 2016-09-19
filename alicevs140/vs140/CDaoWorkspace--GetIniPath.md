---
title: "CDaoWorkspace::GetIniPath"
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
ms.assetid: ff969872-abc1-4aec-ac6a-37e49bd7eca2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::GetIniPath
Call this member function to obtain the location of the Microsoft Jet database engine's initialization settings in the Windows registry.  
  
## Syntax  
  
```  
  
static CString PASCAL GetIniPath( );  
  
```  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) containing the registry location.  
  
## Remarks  
 You can use the location to obtain information about settings for the database engine. The information returned is actually the name of a registry subkey.  
  
 For related information, see the topics "IniPath Property" and "Customizing Windows Registry Settings for Data Access" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoWorkspace::SetIniPath](../vs140/CDaoWorkspace--SetIniPath.md)   
 [CDaoWorkspace::GetVersion](../vs140/CDaoWorkspace--GetVersion.md)