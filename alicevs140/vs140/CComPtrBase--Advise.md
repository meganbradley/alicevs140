---
title: "CComPtrBase::Advise"
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
ms.assetid: c5828188-639b-44f3-b7cf-c923a6910d4e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtrBase::Advise
Call this method to create a connection between the `CComPtrBase`'s connection point and a client's sink.  
  
## Syntax  
  
```  
  
      HRESULT Advise(  
   IUnknown* pUnk,  
   const IID& iid,  
   LPDWORD pdw   
) throw( );  
```  
  
#### Parameters  
 *pUnk*  
 A pointer to the client's **IUnknown**.  
  
 `iid`  
 The GUID of the connection point. Typically, this is the same as the outgoing interface managed by the connection point.  
  
 `pdw`  
 A pointer to the cookie that uniquely identifies the connection.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 See [AtlAdvise](../vs140/AtlAdvise.md) for more information.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)