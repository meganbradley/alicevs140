---
title: "CDataPathProperty::SetControl"
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
ms.assetid: 2a13dd80-a76e-41d2-bbb4-cd5a200b8d60
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataPathProperty::SetControl
Call this member function to associate an asynchronous OLE control with the `CDataPathProperty` object.  
  
## Syntax  
  
```  
  
      void SetControl(  
   COleControl* pControl   
);  
```  
  
#### Parameters  
 `pControl`  
 A pointer to the asynchronous OLE control to be associated with the property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CDataPathProperty Class](../vs140/CDataPathProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataPathProperty::GetControl](../vs140/CDataPathProperty--GetControl.md)   
 [CDataPathProperty::SetPath](../vs140/CDataPathProperty--SetPath.md)   
 [CDataPathProperty::CDataPathProperty](../vs140/CDataPathProperty--CDataPathProperty.md)