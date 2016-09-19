---
title: "CHtmlEditCtrlBase::Copy"
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
ms.assetid: 54788d8f-a769-473d-8fd5-bdf97cb1c9f2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::Copy
Copies the current selection to the clipboard.  
  
## Syntax  
  
```  
  
HRESULT Copy( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_COPY command ID](https://msdn.microsoft.com/en-us/library/aa769872.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::Cut](../vs140/CHtmlEditCtrlBase--Cut.md)   
 [CHtmlEditCtrlBase::Paste](../vs140/CHtmlEditCtrlBase--Paste.md)