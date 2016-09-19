---
title: "IDebugDocumentPositionOffset2::GetRange"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 27da7130-0932-4f97-abde-05e6fb018606
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentPositionOffset2::GetRange
Retrieves the range for the current document position.  
  
## Syntax  
  
```cpp#  
HRESULT GetRange(  
   DWORD* pdwBegOffset,  
   DWORD* pdwEndOffset  
);  
```  
  
```c#  
public int GetRange(  
   ref uint pdwBegOffset,  
   ref uint pdwEndOffset  
);  
```  
  
#### Parameters  
 `pdwBegOffset`  
 [in, out] Offset for the start position of the range. Set this parameter to a null value if this information is not needed.  
  
 `pdwEndOffset`  
 [in, out] Offset for the end position of the range. Set this parameter to a null value if this information is not needed.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The range specified in a document position for a location breakpoint is used by the debug engine (DE) to search ahead for a statement that actually contributes code. For example, consider the following code:  
  
```  
Line 5: // comment  
Line 6: x = 1;  
```  
  
 Line 5 contributes no code to the program being debugged. If the debugger that sets the breakpoint on line 5 wants the DE to search forward a certain amount for the first line that contributes code, the debugger would specify a range that includes additional candidate lines where a breakpoint might be correctly placed. The DE would then search forward through those lines until it found a line that could accept a breakpoint.  
  
## See Also  
 [IDebugDocumentPositionOffset2](../vs140/IDebugDocumentPositionOffset2.md)   
 [IDebugDocumentPosition2::GetRange](../vs140/IDebugDocumentPosition2--GetRange.md)