---
title: "AtlAdvise"
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
ms.assetid: 625a2f03-6b7f-4761-be5d-d2871d1d3254
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlAdvise
Creates a connection between an object's connection point and a client's sink.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      HRESULT AtlAdvise(  
IUnknown* pUnkCP,  
IUnknown* pUnk,  
const IID& iid,  
LPDWORD pdw   
);  
```  
  
#### Parameters  
 `pUnkCP`  
 [in] A pointer to the **IUnknown** of the object the client wants to connect with.  
  
 *pUnk*  
 [in] A pointer to the client's **IUnknown**.  
  
 `iid`  
 [in] The GUID of the connection point. Typically, this is the same as the outgoing interface managed by the connection point.  
  
 `pdw`  
 [out] A pointer to the cookie that uniquely identifies the connection.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 The sink implements the outgoing interface supported by the connection point. The client uses the `pdw` cookie to remove the connection by passing it to [AtlUnadvise](../vs140/AtlUnadvise.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#91](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#91)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Connection Point Global Functions](../vs140/Connection-Point-Global-Functions.md)