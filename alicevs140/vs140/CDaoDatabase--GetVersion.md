---
title: "CDaoDatabase::GetVersion"
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
ms.assetid: f31a2b78-7fc0-430b-9617-dc13ce75dc99
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::GetVersion
Call this member function to determine the version of the Microsoft Jet database file.  
  
## Syntax  
  
```  
  
CString GetVersion( );  
  
```  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) that indicates the version of the database file associated with the object.  
  
## Remarks  
 The value returned represents the version number in the form "major.minor"; for example, "3.0". The product version number (for example, 3.0) consists of the version number (3), a period, and the release number (0). The versions to date are 1.0, 1.1, 2.0, and 3.0.  
  
 For related information, see the topic "Version Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)