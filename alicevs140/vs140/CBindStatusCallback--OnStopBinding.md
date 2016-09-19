---
title: "CBindStatusCallback::OnStopBinding"
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
ms.assetid: da3e4a90-529a-47b3-af2a-b6188ade541a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::OnStopBinding
Releases the `IBinding` pointer in the data member [m_spBinding](../vs140/CBindStatusCallback--m_spBinding.md).  
  
## Syntax  
  
```  
  
      STDMETHOD(OnStopBinding)(  
   HRESULT hresult,  
   LPCWSTR /* szError */   
);  
```  
  
#### Parameters  
 `hresult`  
 Status code returned from the bind operation.  
  
 szStatusText  
 Address of a string value Unused.  
  
## Remarks  
 Called by the system-supplied asynchronous moniker to indicate the end of the bind operation.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::OnStartBinding](../vs140/CBindStatusCallback--OnStartBinding.md)