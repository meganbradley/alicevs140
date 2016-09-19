---
title: "CHtmlEditCtrlBase::GetDocumentHTML"
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
ms.assetid: 72f9782b-8b96-448a-8d58-7fb169ade06e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetDocumentHTML
Retrieves the HTML of the current document.  
  
## Syntax  
  
```  
  
      HRESULT GetDocumentHTML(  
   CString& szHTML   
) const;  
```  
  
#### Parameters  
 `szHTML`  
 The HTML.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetDocumentHTML](../vs140/CHtmlEditCtrlBase--SetDocumentHTML.md)