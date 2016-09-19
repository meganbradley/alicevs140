---
title: "COleObjectFactory::OnCreateObject"
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
ms.assetid: 13095e89-8ab0-4bdb-9e99-6c338ecee07e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::OnCreateObject
Called by the framework to create a new object.  
  
## Syntax  
  
```  
  
virtual CCmdTarget* OnCreateObject( );  
```  
  
## Return Value  
 A pointer to the created object. It can throw a memory exception if it fails.  
  
## Remarks  
 Override this function to create the object from something other than the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) passed to the constructor.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::COleObjectFactory](../vs140/COleObjectFactory--COleObjectFactory.md)   
 [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md)