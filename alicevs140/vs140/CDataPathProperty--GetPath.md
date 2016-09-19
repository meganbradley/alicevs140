---
title: "CDataPathProperty::GetPath"
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
ms.assetid: 0090c54f-e5b7-4acf-9878-5174851f4f19
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataPathProperty::GetPath
Call this member function to retrieve the path, set when the `CDataPathProperty` object was constructed, or specified in **Open**, or specified in a previous call to the `SetPath` member function.  
  
## Syntax  
  
```  
  
CString GetPath( ) const;  
```  
  
## Return Value  
 Returns the pathname to the property itself. Can be empty if no path has been specified.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CDataPathProperty Class](../vs140/CDataPathProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataPathProperty::SetPath](../vs140/CDataPathProperty--SetPath.md)   
 [CDataPathProperty::Open](../vs140/CDataPathProperty--Open.md)   
 [CDataPathProperty::CDataPathProperty](../vs140/CDataPathProperty--CDataPathProperty.md)