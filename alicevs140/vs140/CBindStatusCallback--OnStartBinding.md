---
title: "CBindStatusCallback::OnStartBinding"
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
ms.assetid: dd21f766-d2ec-4498-857d-ea7fc17f3842
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::OnStartBinding
Sets the data member [m_spBinding](../vs140/CBindStatusCallback--m_spBinding.md) to the `IBinding` pointer in `pBinding`.  
  
## Syntax  
  
```  
  
      STDMETHOD(OnStartBinding)(  
   DWORD /* dwReserved */,  
   IBinding* pBinding   
);  
```  
  
#### Parameters  
 `dwReserved`  
 Reserved for future use.  
  
 `pBinding`  
 [in] Address of the IBinding interface of the current bind operation. This cannot be NULL. The client should call AddRef on this pointer to keep a reference to the binding object.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::OnStopBinding](../vs140/CBindStatusCallback--OnStopBinding.md)