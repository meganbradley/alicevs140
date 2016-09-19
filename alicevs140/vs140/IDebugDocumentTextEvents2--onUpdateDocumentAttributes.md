---
title: "IDebugDocumentTextEvents2::onUpdateDocumentAttributes"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 31b7d151-9ce2-438e-b405-f8cc46b9f537
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentTextEvents2::onUpdateDocumentAttributes
Notifies receiver of the event that the document attributes have been updated.  
  
## Syntax  
  
```cpp#  
HRESULT onUpdateDocumentAttributes(   
   TEXT_DOC_ATTR_2 textdocattr  
);  
```  
  
```c#  
int onUpdateDocumentAttributes(   
   enum_TEXT_DOC_ATTR_2 textdocattr  
);  
```  
  
#### Parameters  
 `textdocattr`  
 [in] A combination of flags from the [TEXT_DOC_ATTR_2](../vs140/TEXT_DOC_ATTR_2.md) enumeration that specifies the updated attributes of the document.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugDocumentTextEvents2](../Topic/IDebugDocumentTextEvents2.md)   
 [TEXT_DOC_ATTR_2](../vs140/TEXT_DOC_ATTR_2.md)