---
title: "CHtmlEditCtrlBase::Underline"
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
ms.assetid: a02caae5-41b5-43e0-9ad2-2afd5aea6529
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::Underline
Toggles the current selection between underlined and not underlined.  
  
## Syntax  
  
```  
  
HRESULT Underline( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM UNDERLINE command ID](https://msdn.microsoft.com/en-us/library/aa770035.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::Bold](../vs140/CHtmlEditCtrlBase--Bold.md)   
 [CHtmlEditCtrlBase::Italic](../vs140/CHtmlEditCtrlBase--Italic.md)