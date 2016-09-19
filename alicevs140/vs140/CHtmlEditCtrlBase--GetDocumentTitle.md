---
title: "CHtmlEditCtrlBase::GetDocumentTitle"
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
ms.assetid: e4291b63-4682-431a-afc7-d4a73ba86fbb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetDocumentTitle
Retrieves the document's title.  
  
## Syntax  
  
```  
  
      HRESULT GetDocumentTitle(  
   CString& szTitle   
) const;  
```  
  
#### Parameters  
 *szTitle*  
 The document's title.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)