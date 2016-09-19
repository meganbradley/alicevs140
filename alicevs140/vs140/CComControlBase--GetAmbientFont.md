---
title: "CComControlBase::GetAmbientFont"
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
ms.assetid: 012aeb2e-e925-43b8-a3b8-271912144279
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientFont
Retrieves a pointer to the container's ambient `IFont` interface.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientFont(  
   IFont** ppFont   
);  
```  
  
#### Parameters  
 `ppFont`  
 A pointer to the container's ambient [IFont](http://msdn.microsoft.com/library/windows/desktop/ms680673) interface.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Remarks  
 If the property is **NULL**, the pointer is **NULL**. If the pointer is not **NULL**, the caller must release the pointer.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)