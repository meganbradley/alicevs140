---
title: "CDaoWorkspace::GetVersion"
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
ms.assetid: 111461d3-9e3b-4348-acb3-15ae8731372f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::GetVersion
Call this member function to determine the version of the Microsoft Jet database engine in use.  
  
## Syntax  
  
```  
  
static CString PASCAL GetVersion( );  
  
```  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) that indicates the version of the database engine associated with the object.  
  
## Remarks  
 The value returned represents the version number in the form "major.minor"; for example, "3.0". The product version number (for example, 3.0) consists of the version number (3), a period, and the release number (0).  
  
 For related information, see the topic "Version Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoDatabase::GetVersion](../vs140/CDaoDatabase--GetVersion.md)