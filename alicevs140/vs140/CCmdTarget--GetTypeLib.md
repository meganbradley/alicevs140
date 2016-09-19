---
title: "CCmdTarget::GetTypeLib"
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
ms.assetid: 66c08e0f-3d7e-4ab8-b4f0-b17b969f12de
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::GetTypeLib
Gets a pointer to a type library.  
  
## Syntax  
  
```  
  
      virtual HRESULT GetTypeLib(  
   LCID lcid,  
   LPTYPELIB* ppTypeLib   
);  
```  
  
#### Parameters  
 `lcid`  
 A locale identifier (`LCID`).  
  
 `ppTypeLib`  
 A pointer to a pointer to the `ITypeLib` interface.  
  
## Return Value  
 An HRESULT indicating the success or failure of the call. If successful, *`ppTypeLib` points to the type library interface.  
  
## Remarks  
 Derived classes should override this member function (if not overridden, `GetTypeLib` returns TYPE_E_CANTLOADLIBRARY). Use the [IMPLEMENT_OLETYPELIB](../vs140/IMPLEMENT_OLETYPELIB.md) macro, which also implements `GetTypeInfoCount` and `GetTypeLibCache`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdTarget::GetTypeInfoCount](../vs140/CCmdTarget--GetTypeInfoCount.md)   
 [CCmdTarget::GetTypeLibCache](../vs140/CCmdTarget--GetTypeLibCache.md)