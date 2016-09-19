---
title: "IDebugDocumentPosition2::IsPositionInDocument"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d5cf57cb-b93b-4e1d-bec9-185f4fe8668d
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentPosition2::IsPositionInDocument
Determines if the document position is contained in the given document.  
  
## Syntax  
  
```cpp#  
HRESULT IsPositionInDocument(   
   IDebugDocument2* pDoc  
);  
```  
  
```c#  
int IsPositionInDocument(   
   IDebugDocument2 pDoc  
);  
```  
  
#### Parameters  
 `pDoc`  
 [in] The [IDebugDocument2](../vs140/IDebugDocument2.md) object that represents the containing document candidate.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method is used primarily in setting breakpoints in [IDebugDocument2](../vs140/IDebugDocument2.md) interfaces. As documents are loaded, the breakpoint position is called to determine if the document contains this position.  
  
## See Also  
 [IDebugDocumentPosition2](../vs140/IDebugDocumentPosition2.md)   
 [IDebugDocument2](../vs140/IDebugDocument2.md)