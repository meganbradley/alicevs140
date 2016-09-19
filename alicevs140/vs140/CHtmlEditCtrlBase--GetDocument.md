---
title: "CHtmlEditCtrlBase::GetDocument"
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
ms.topic: reference
ms.assetid: 0c4d1f13-02be-48f3-92ad-2d3715438e89
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetDocument
Retrieves the document object.  
  
## Syntax  
  
```  
  
      HRESULT GetDocument(  
   IHTMLDocument2** ppDoc   
) const;  
```  
  
#### Parameters  
 `ppDoc`  
 The document object.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)