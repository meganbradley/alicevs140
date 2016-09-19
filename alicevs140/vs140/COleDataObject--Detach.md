---
title: "COleDataObject::Detach"
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
ms.assetid: e83a01bc-9e6f-4214-8022-c854e3181f3f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataObject::Detach
Call this function to detach the `COleDataObject` object from its associated OLE data object without releasing the data object.  
  
## Syntax  
  
```  
  
LPDATAOBJECT Detach( );  
```  
  
## Return Value  
 A pointer to the OLE data object that was detached.  
  
## Remarks  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject::Attach](../vs140/COleDataObject--Attach.md)   
 [COleDataObject::Release](../vs140/COleDataObject--Release.md)