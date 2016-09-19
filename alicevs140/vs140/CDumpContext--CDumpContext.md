---
title: "CDumpContext::CDumpContext"
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
ms.assetid: 6cb7f7a1-3b67-4cdb-b27e-3f1453772eb7
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDumpContext::CDumpContext
Constructs an object of class `CDumpContext`.  
  
## Syntax  
  
```  
  
      CDumpContext(  
   CFile* pFile = NULL  
);  
```  
  
#### Parameters  
 `pFile`  
 A pointer to the `CFile` object that is the dump destination.  
  
## Remarks  
 The `afxDump` object is constructed automatically.  
  
 Do not write to the underlying `CFile` while the dump context is active; otherwise, you will interfere with the dump. Under the Windows environment, the output is routed to the debugger via the Windows function **OutputDebugString**.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#12)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CDumpContext Class](../vs140/CDumpContext-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)