---
title: "CDataPathProperty::SetPath"
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
ms.assetid: 45d7417b-452e-4897-91fb-c62ea7896c18
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataPathProperty::SetPath
Call this member function to set the pathname of the property.  
  
## Syntax  
  
```  
  
      void SetPath(  
   LPCTSTR lpszPath   
);  
```  
  
#### Parameters  
 `lpszPath`  
 A path, which may be absolute or relative, to the property being loaded asynchronously. `CDataPathProperty` uses URLs, not filenames. If you want a `CDataPathProperty` object for a file, prepend `file://` to the path.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CDataPathProperty Class](../vs140/CDataPathProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataPathProperty::GetPath](../vs140/CDataPathProperty--GetPath.md)   
 [CDataPathProperty::SetControl](../vs140/CDataPathProperty--SetControl.md)   
 [CDataPathProperty::CDataPathProperty](../vs140/CDataPathProperty--CDataPathProperty.md)