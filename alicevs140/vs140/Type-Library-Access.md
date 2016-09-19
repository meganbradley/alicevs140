---
title: "Type Library Access"
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
ms.topic: article
ms.assetid: a03fa7f0-86c2-4119-bf81-202916fb74b3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type Library Access
Type libraries expose the interfaces of an OLE control to other OLE-aware applications. Each OLE control must have a type library if one or more interfaces are to be exposed.  
  
 The following macros allow an OLE control to provide access to its own type library:  
  
### Type Library Access  
  
|||  
|-|-|  
|[DECLARE_OLETYPELIB](../vs140/DECLARE_OLETYPELIB.md)|Declares a `GetTypeLib` member function of an OLE control (must be used in the class declaration).|  
|[IMPLEMENT_OLETYPELIB](../vs140/IMPLEMENT_OLETYPELIB.md)|Implements a `GetTypeLib` member function of an OLE control (must be used in the class implementation).|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)