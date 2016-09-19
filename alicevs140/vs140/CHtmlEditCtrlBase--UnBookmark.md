---
title: "CHtmlEditCtrlBase::UnBookmark"
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
ms.assetid: d8ac5e4f-30a2-428c-9c5e-f18041cb73c3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::UnBookmark
Removes any bookmark from the current selection.  
  
## Syntax  
  
```  
  
HRESULT UnBookmark( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM UNBOOKMARK command ID](https://msdn.microsoft.com/en-us/library/aa770034.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetBookMark](../vs140/CHtmlEditCtrlBase--SetBookMark.md)   
 [CHtmlEditCtrlBase::GetBookMark](../vs140/CHtmlEditCtrlBase--GetBookMark.md)