---
title: "CGopherFileFind::GetLocator"
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
ms.assetid: 82822a3d-7f0b-4b4d-86e3-401e68aeabdd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherFileFind::GetLocator
Call this member function to get the [CGopherLocator](../vs140/CGopherLocator-Class.md) object that [FindFile](../vs140/CGopherFileFind--FindFile.md) uses to find the gopher file.  
  
## Syntax  
  
```  
  
CGopherLocator GetLocator( ) const;  
  
```  
  
## Return Value  
 A `CGopherLocator` object.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CGopherFileFind Class](../vs140/CGopherFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGopherConnection::CreateLocator](../vs140/CGopherConnection--CreateLocator.md)