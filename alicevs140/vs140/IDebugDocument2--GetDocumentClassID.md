---
title: "IDebugDocument2::GetDocumentClassID"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 111c2b85-ebfa-487f-b896-2ec4a3eac4d1
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocument2::GetDocumentClassID
Gets the class identifier of the document.  
  
## Syntax  
  
```cpp#  
HRESULT GetDocumentClassID(   
   CLSID* pclsid  
);  
```  
  
```c#  
int GetDocumentClassID(   
   out Guid pclsid  
);  
```  
  
#### Parameters  
 `pclsid`  
 [out] Returns a GUID that is the class ID of the document.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The class GUID can be used to instantiate individual classes each of which represents a document.  
  
## See Also  
 [IDebugDocument2](../vs140/IDebugDocument2.md)