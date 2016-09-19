---
title: "Callback Function for CDC::SetAbortProc"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: daa36d5d-15de-40fc-8d37-a865d06c4710
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Callback Function for CDC::SetAbortProc
The name *AbortFunc* is a placeholder for the application-supplied function name.  
  
## Syntax  
  
```  
  
      BOOL CALLBACK EXPORT AbortFunc(   
   HDC hPr,   
   int code    
);  
```  
  
#### Parameters  
 *hPr*  
 Identifies the device context.  
  
 `code`  
 Specifies whether an error has occurred. It is 0 if no error has occurred. It is **SP_OUTOFDISK** if the Print Manager is currently out of disk space and more disk space will become available if the application waits. If `code` is **SP_OUTOFDISK**, the application does not have to abort the print job. If it does not, it must yield to the Print Manager by calling the **PeekMessage** or **GetMessage** Windows function.  
  
## Return Value  
 The return value of the abort-handler function is nonzero if the print job is to continue, and 0 if it is canceled.  
  
## Remarks  
 The actual name must be exported as described in the Remarks section of [CDC::SetAbortProc](../vs140/CDC--SetAbortProc.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CDC::SetAbortProc](../vs140/CDC--SetAbortProc.md)