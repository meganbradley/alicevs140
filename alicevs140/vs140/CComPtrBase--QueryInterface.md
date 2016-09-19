---
title: "CComPtrBase::QueryInterface"
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
ms.assetid: 6fd63bcb-0b7c-4d24-a281-b89805e74f81
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtrBase::QueryInterface
Call this method to return a pointer to a specified interface.  
  
## Syntax  
  
```  
  
      template <  
   class Q  
> HRESULT QueryInterface(Q** pp ) const throw( );  
```  
  
#### Parameters  
 `Q`  
 The object type whose interface pointer is required.  
  
 `pp`  
 Address of output variable that receives the requested interface pointer.  
  
## Return Value  
 Returns S_OK on success, or E_NOINTERFACE on failure.  
  
## Remarks  
 This method calls [IUnknown::QueryInterface](http://msdn.microsoft.com/library/windows/desktop/ms682521).  
  
 In debug builds, an assertion error will occur if *pp* is not equal to NULL.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)   
 [CComPtrBase::SetSite](../vs140/CComPtrBase--SetSite.md)