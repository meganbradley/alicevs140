---
title: "IDebugBreakpointChecksumRequest2::IsChecksumEnabled"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8b1853b5-745c-4cd6-88a9-ce0673971bb0
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointChecksumRequest2::IsChecksumEnabled
Determines whether the checksum is enabled for this document.  
  
## Syntax  
  
```cpp#  
HRESULT IsChecksumEnabled(   
   BOOL *pfChecksumEnabled  
);  
```  
  
```c#  
public int IsChecksumEnabled(   
   out int pfChecksumEnabled  
);  
```  
  
#### Parameters  
 `pfChecksumEnabled`  
 [out] Returns TRUE if the checksum is enabled; otherwise, returns FALSE.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugBreakpointChecksumRequest2](../vs140/IDebugBreakpointChecksumRequest2.md)