---
title: "CHtmlEditCtrlBase::IE50Paste"
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
ms.assetid: 804327a0-b354-42fd-b774-03e80178be15
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::IE50Paste
Performs a paste operation that's compatible with Internet Explorer 5.  
  
## Syntax  
  
```  
  
      HRESULT IE50Paste(  
   LPCTSTR szData   
) const;  
```  
  
#### Parameters  
 `szData`  
 The string to paste.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_IE50_PASTE command ID](https://msdn.microsoft.com/en-us/library/aa769922.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetIE5PasteMode](../vs140/CHtmlEditCtrlBase--SetIE5PasteMode.md)