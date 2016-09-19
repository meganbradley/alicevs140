---
title: "IDebugDocumentContext2::Seek"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71501356-8a82-4d36-b354-6625bdd2baa0
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentContext2::Seek
Moves the document context by a given number of statements or lines.  
  
## Syntax  
  
```cpp#  
HRESULT Seek(   
   int                      nCount,  
   IDebugDocumentContext2** ppDocContext  
);  
```  
  
```cpp#  
int Seek(   
   int                        nCount,  
   out IDebugDocumentContext2 ppDocContext  
);  
```  
  
#### Parameters  
 `nCount`  
 [in] The number of statements or lines to move ahead, depending on the document context.  
  
 `ppDocContext`  
 [out] Returns a new [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md) object with the new position.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md)