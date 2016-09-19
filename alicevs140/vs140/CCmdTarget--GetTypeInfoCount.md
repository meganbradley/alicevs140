---
title: "CCmdTarget::GetTypeInfoCount"
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
ms.assetid: fe71e6d6-4773-43cb-b818-e642d4bbe8fb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::GetTypeInfoCount
Retrieves the number of type information interfaces that an object provides.  
  
## Syntax  
  
```  
  
virtual UINT GetTypeInfoCount( );  
```  
  
## Return Value  
 The number of type information interfaces.  
  
## Remarks  
 This member function basically implements [IDispatch::GetTypeInfoCount](assetId:///da876d53-cb8a-465c-a43e-c0eb272e2a12).  
  
 Derived classes should override this function to return the number of type information interfaces provided (either 0 or 1). If not overridden, **GetTypeInfoCount** returns 0. To override, use the [IMPLEMENT_OLETYPELIB](../vs140/IMPLEMENT_OLETYPELIB.md) macro, which also implements `GetTypeLib` and `GetTypeLibCache`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdTarget::GetTypeLib](../vs140/CCmdTarget--GetTypeLib.md)   
 [CCmdTarget::GetTypeLibCache](../vs140/CCmdTarget--GetTypeLibCache.md)