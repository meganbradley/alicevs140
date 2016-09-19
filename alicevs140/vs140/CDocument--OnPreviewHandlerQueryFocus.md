---
title: "CDocument::OnPreviewHandlerQueryFocus"
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
ms.assetid: 38a47c06-a065-4b64-bd5f-677ff05cfd3f
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnPreviewHandlerQueryFocus
Directs the preview handler to return the HWND retrieved from calling the `GetFocus` function.  
  
## Syntax  
  
```  
virtual HRESULT OnPreviewHandlerQueryFocus(  
   HWND* phwnd  
);  
```  
  
#### Parameters  
 `phwnd`  
 [out] When this method returns, contains a pointer to the HWND returned from calling the `GetFocus` function from the preview handler's foreground thread.  
  
## Return Value  
 Returns S_OK if successful; or an error value otherwise.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)