---
title: "CGopherLocator::CGopherLocator"
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
ms.assetid: 1f5e9056-c37a-43f9-9eb3-b438de52462e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherLocator::CGopherLocator
This member function is called to create a `CGopherLocator` object.  
  
## Syntax  
  
```  
  
      CGopherLocator(  
   const CGopherLocator& ref   
);  
```  
  
#### Parameters  
 `ref`  
 A reference to a constant `CGopherLocator` object.  
  
## Remarks  
 You never create a `CGopherLocator` object directly. Instead, call [CGopherConnection::CreateLocator](../vs140/CGopherConnection--CreateLocator.md) to create and return a pointer to the `CGopherLocator` object.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CGopherLocator Class](../vs140/CGopherLocator-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGopherFileFind Class](../vs140/CGopherFileFind-Class.md)   
 [CGopherConnection Class](../vs140/CGopherConnection-Class.md)