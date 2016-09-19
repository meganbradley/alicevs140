---
title: "AtlAdviseSinkMap"
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
ms.assetid: 0757a6af-3de3-4179-8b4f-ccd137d919b4
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlAdviseSinkMap
Call this function to advise or unadvise all entries in the object's sink event map.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      HRESULT AtlAdviseSinkMap(  
T* pT,  
bool bAdvise   
);  
```  
  
#### Parameters  
 *pT*  
 [in] A pointer to the object containing the sink map.  
  
 `bAdvise`  
 [in] **true** if all sink entries are to be advised; **false** if all sink entries are to be unadvised.  
  
## Return Value  
 A standard HRESULT value.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#92](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#92)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Connection Point Global Functions](../vs140/Connection-Point-Global-Functions.md)