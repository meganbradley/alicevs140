---
title: "AtlUnadvise"
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
ms.assetid: 939d2e50-e2df-4e8f-a16a-e9650b8f0340
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlUnadvise
Terminates the connection established through [AtlAdvise](../vs140/AtlAdvise.md).  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      HRESULT AtlUnadvise(  
IUnknown* pUnkCP,  
const IID& iid,  
DWORD dw   
);  
```  
  
#### Parameters  
 `pUnkCP`  
 [in] A pointer to the **IUnknown** of the object that the client is connected with.  
  
 `iid`  
 [in] The GUID of the connection point. Typically, this is the same as the outgoing interface managed by the connection point.  
  
 `dw`  
 [in] The cookie that uniquely identifies the connection.  
  
## Return Value  
 A standard HRESULT value.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#96](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#96)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Connection Point Global Functions](../vs140/Connection-Point-Global-Functions.md)