---
title: "IDebugDocumentPosition2::GetFileName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d713635e-088f-465b-b26d-00ac971c9e86
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentPosition2::GetFileName
Gets the file name of the source file that contains the document position.  
  
## Syntax  
  
```cpp#  
HRESULT GetFileName(   
   BSTR* pbstrFileName  
);  
```  
  
```c#  
int GetFileName(   
   out string pbstrFileName  
);  
```  
  
#### Parameters  
 `pbstrFileName`  
 [out] Returns the file name of the source file.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 A source file may not always have a file name (the source file may not exist on disk, for example).  
  
## See Also  
 [IDebugDocumentPosition2](../vs140/IDebugDocumentPosition2.md)