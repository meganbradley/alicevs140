---
title: "CCachedDataPathProperty::CCachedDataPathProperty"
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
ms.assetid: a8bbb508-4f36-4175-a5fd-06524f500a95
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCachedDataPathProperty::CCachedDataPathProperty
Constructs a `CCachedDataPathProperty` object.  
  
## Syntax  
  
```  
  
      CCachedDataPathProperty(  
   COleControl* pControl = NULL  
);  
CCachedDataPathProperty(  
   LPCTSTR lpszPath,  
   COleControl* pControl = NULL  
);  
```  
  
#### Parameters  
 `pControl`  
 A pointer to the ActiveX control object to be associated with this `CCachedDataPathProperty` object.  
  
 `lpszPath`  
 The path, which may be absolute or relative, used to create an asynchronous moniker that references the actual absolute location of the property. `CCachedDataPathProperty` uses URLs, not filenames. If you want a `CCachedDataPathProperty` object for a file, prepend file:// to the path.  
  
## Remarks  
 The `COleControl` object pointed to by `pControl` is used by [Open](../vs140/CDataPathProperty--Open.md) and retrieved by derived classes. If `pControl` is **NULL**, the control used with **Open** should be set with [SetControl](../vs140/CDataPathProperty--SetControl.md). If `lpszPath` is **NULL**, you can pass in the path through **Open** or set it with [SetPath](../vs140/CDataPathProperty--SetPath.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CCachedDataPathProperty Class](../vs140/CCachedDataPathProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataPathProperty Class](../vs140/CDataPathProperty-Class.md)