---
title: "IDebugDocumentText2::GetSize"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bf515a8f-dcee-4004-8f81-543d547ceaae
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentText2::GetSize
Retrieves the size of the text at this position in the document.  
  
## Syntax  
  
```cpp#  
HRESULT GetSize(   
   ULONG* pcNumLines,  
   ULONG* pcNumChars  
);  
```  
  
```c#  
int GetSize(   
   ref uint pcNumLines,  
   ref uint pcNumChars  
);  
```  
  
#### Parameters  
 `pcNumLines`  
 [out] Returns the number of lines of text.  
  
 `pcNumChars`  
 [out] Returns the number of characters of text.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 [C++ only] If a particular value is not desired, pass a NULL for the parameter.  
  
 [C# only] Both parameters must be specified.  
  
## See Also  
 [IDebugDocumentText2](../Topic/IDebugDocumentText2.md)