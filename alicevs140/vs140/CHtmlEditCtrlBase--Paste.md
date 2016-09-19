---
title: "CHtmlEditCtrlBase::Paste"
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
ms.assetid: ffb7d5e2-6938-4d7c-bb16-bc58fa190ff9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::Paste
Overwrites the contents of the clipboard on the current selection.  
  
## Syntax  
  
```  
  
HRESULT Paste( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_PASTE command ID](https://msdn.microsoft.com/en-us/library/aa770017.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::Copy](../vs140/CHtmlEditCtrlBase--Copy.md)   
 [CHtmlEditCtrlBase::Cut](../vs140/CHtmlEditCtrlBase--Cut.md)   
 [CHtmlEditCtrlBase::IE50Paste](../vs140/CHtmlEditCtrlBase--IE50Paste.md)