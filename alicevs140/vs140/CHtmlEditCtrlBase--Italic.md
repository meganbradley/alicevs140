---
title: "CHtmlEditCtrlBase::Italic"
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
ms.assetid: 75aac510-6d9c-4581-95a6-852260bcd60d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::Italic
Toggles the current selection between italic and nonitalic.  
  
## Syntax  
  
```  
  
HRESULT Italic( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_ITALIC command ID](https://msdn.microsoft.com/en-us/library/aa769988.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::Bold](../vs140/CHtmlEditCtrlBase--Bold.md)   
 [CHtmlEditCtrlBase::Underline](../vs140/CHtmlEditCtrlBase--Underline.md)