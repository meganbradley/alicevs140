---
title: "IDebugDocumentTextEvents2::onInsertText"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6040181f-7288-4a42-953c-d23f74200431
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentTextEvents2::onInsertText
Notifies the debug package that text has been inserted into the document.  
  
## Syntax  
  
```cpp#  
HRESULT onInsert(   
   TEXT_POSITION pos,  
   DWORD         dwNumToInsert  
);  
```  
  
```c#  
int onInsert(   
   enum_TEXT_POSITION pos,  
   uint               dwNumToInsert  
);  
```  
  
#### Parameters  
 `pos`  
 [in] A [TEXT_POSITION](../vs140/TEXT_POSITION.md) structure that indicates where the text was inserted.  
  
 `dwNumToInsert`  
 [in] Specifies the number of characters of text that were inserted.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugDocumentTextEvents2](../Topic/IDebugDocumentTextEvents2.md)   
 [TEXT_POSITION](../vs140/TEXT_POSITION.md)