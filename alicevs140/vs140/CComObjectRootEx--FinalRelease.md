---
title: "CComObjectRootEx::FinalRelease"
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
ms.assetid: 52481a2e-e5f8-4fad-9814-362e62f4eed9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRootEx::FinalRelease
You can override this method in your derived class to perform any cleanup required for your object.  
  
## Syntax  
  
```  
  
void FinalRelease( );  
```  
  
## Remarks  
 By default, `CComObjectRootEx::FinalRelease` does nothing.  
  
 Performing cleanup in `FinalRelease` is preferable to adding code to the destructor of your class since the object is still fully constructed at the point at which `FinalRelease` is called. This enables you to safely access the methods provided by the most derived class. This is particularly important for freeing any aggregated objects before deletion.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComObjectRootEx::FinalConstruct](../vs140/CComObjectRootEx--FinalConstruct.md)