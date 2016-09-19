---
title: "CDocument::OnLoadDocumentFromStream"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 4d1f079a-4167-487c-bd3b-8cb9054b27fa
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnLoadDocumentFromStream
Called by the framework when it needs to load the document data from a stream.  
  
## Syntax  
  
```  
virtual HRESULT OnLoadDocumentFromStream(  
   IStream* pStream,  
   DWORD grfMode  
);  
```  
  
#### Parameters  
 `pStream`  
 A pointer to an incoming stream.  
  
 `grfMode`  
 Access mode to the stream.  
  
## Return Value  
 S_OK if the load is successful; otherwise an error code.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)