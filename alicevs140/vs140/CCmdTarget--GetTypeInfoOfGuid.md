---
title: "CCmdTarget::GetTypeInfoOfGuid"
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
ms.assetid: 5fb3160c-2f45-442a-bf06-017a3fffa31c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::GetTypeInfoOfGuid
Retrieves the type description that corresponds to the specified GUID.  
  
## Syntax  
  
```  
  
      HRESULT GetTypeInfoOfGuid(  
   LCID lcid,  
   const GUID& guid,  
   LPTYPEINFO* ppTypeInfo   
);  
```  
  
#### Parameters  
 `lcid`  
 A locale identifier (`LCID`).  
  
 `guid`  
 The [GUID](http://msdn.microsoft.com/library/windows/desktop/aa373931) of the type description.  
  
 `ppTypeInfo`  
 Pointer to a pointer to the `ITypeInfo` interface.  
  
## Return Value  
 An HRESULT indicating the success or failure of the call. If successful, *`ppTypeInfo` points to the type information interface.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)