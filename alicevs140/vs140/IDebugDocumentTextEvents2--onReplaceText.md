---
title: "IDebugDocumentTextEvents2::onReplaceText"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cb39f025-66d8-4dc0-bef6-1bdc8e07db92
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentTextEvents2::onReplaceText
Notifies the debug package that text has been replaced in the document.  
  
## Syntax  
  
```cpp#  
HRESULT onReplaceText(   
   TEXT_POSITION pos,  
   DWORD         dwNumToReplace  
);  
```  
  
```c#  
int onReplaceText(   
   enum_TEXT_POSITION pos,  
   uint               dwNumToReplace  
);  
```  
  
#### Parameters  
 `pos`  
 [in] A [TEXT_POSITION](../vs140/TEXT_POSITION.md) indicates where the text was replaced.  
  
 `dwNumToReplace`  
 [in] Specifies the number of characters of text that were replaced.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugDocumentTextEvents2](../Topic/IDebugDocumentTextEvents2.md)   
 [TEXT_POSITION](../vs140/TEXT_POSITION.md)