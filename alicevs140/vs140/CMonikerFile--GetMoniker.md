---
title: "CMonikerFile::GetMoniker"
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
ms.assetid: 62d2dbbb-7120-4c92-9cff-72a6939337a5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonikerFile::GetMoniker
Call this function to retrieve a pointer to the current moniker.  
  
## Syntax  
  
```  
  
IMoniker* GetMoniker( ) const;  
```  
  
## Return Value  
 A pointer to the current moniker interface ([IMoniker](http://msdn.microsoft.com/library/windows/desktop/ms679705)).  
  
## Remarks  
 Since `CMonikerFile` is not an interface, the pointer returned does not increment the reference count (through [AddRef](http://msdn.microsoft.com/library/windows/desktop/ms691379)), and the moniker is released when the `CMonikerFile` object is released. If you want to hold onto the moniker or release it yourself, you must `AddRef` it.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CMonikerFile Class](../vs140/CMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)