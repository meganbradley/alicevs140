---
title: "CComObjectStack::CComObjectStack"
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
ms.assetid: bdb86124-114d-4e6d-9a19-2d5442ec79d5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectStack::CComObjectStack
The constructor.  
  
## Syntax  
  
```  
  
      CComObjectStack(  
   void* = NULL   
);  
```  
  
## Remarks  
 Calls `FinalConstruct` and then sets [m_hResFinalConstruct](../vs140/CComObjectStack--m_hResFinalConstruct.md) to the `HRESULT` returned by `FinalConstruct`. If you have not derived your base class from [CComObjectRoot](../vs140/CComObjectRoot-Class.md), you must supply your own `FinalConstruct` method. The destructor calls `FinalRelease`.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectStack Class](../vs140/CComObjectStack-Class.md)   
 [CComObjectRootEx::FinalConstruct](../vs140/CComObjectRootEx--FinalConstruct.md)