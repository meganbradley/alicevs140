---
title: "CDataPathProperty::GetControl"
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
ms.assetid: f0b2ae7b-b61a-4ffa-95df-6e66c88fe37a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataPathProperty::GetControl
Call this member function to retrieve the `COleControl` object associated with the `CDataPathProperty` object.  
  
## Syntax  
  
```  
  
COleControl* GetControl( );  
```  
  
## Return Value  
 Returns a pointer to the OLE control associated with the `CDataPathProperty` object. **NULL** if not control is associated.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CDataPathProperty Class](../vs140/CDataPathProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataPathProperty::SetControl](../vs140/CDataPathProperty--SetControl.md)