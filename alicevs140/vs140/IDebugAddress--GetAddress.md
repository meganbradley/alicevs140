---
title: "IDebugAddress::GetAddress"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2590387b-5d36-4116-9a75-737957b8898e
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugAddress::GetAddress
Returns a structure describing an object and its location within its scope or container.  
  
## Syntax  
  
```cpp  
HRESULT GetAddress (  
   DEBUG_ADDRESS * pAddress  
);  
```  
  
```c#  
int GetAddress(  
   DEBUG_ADDRESS[] pAddress  
);  
```  
  
#### Parameters  
 `pAddress`  
 [in, out] A [DEBUG_ADDRESS](../vs140/DEBUG_ADDRESS.md) structure that is filled in by this method.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 The [DEBUG_ADDRESS](../vs140/DEBUG_ADDRESS.md) structure is passed to this method, which then fills it in with the appropriate information. How this information is interpreted depends on the kind of information returned and the symbol handler itself. See [DEBUG_ADDRESS](../vs140/DEBUG_ADDRESS.md) for more details.  
  
## See Also  
 [DEBUG_ADDRESS](../vs140/DEBUG_ADDRESS.md)