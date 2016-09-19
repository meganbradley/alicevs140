---
title: "IThreadPoolConfig::GetSize"
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
ms.assetid: 984c8a78-5692-4771-b602-64185589629c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IThreadPoolConfig::GetSize
Call this method to get the number of threads in the pool.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetSize)(  
   int * pnNumThreads   
);  
```  
  
#### Parameters  
 `pnNumThreads`  
 [out] Address of the variable that, on success, receives the number of threads in the pool.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#134](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#134)]  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [IThreadPoolConfig Interface](../vs140/IThreadPoolConfig-Interface.md)   
 [IThreadPoolConfig::SetSize](../vs140/IThreadPoolConfig--SetSize.md)