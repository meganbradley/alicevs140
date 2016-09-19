---
title: "CHtmlEditCtrlBase::SetIE5PasteMode"
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
ms.assetid: 4243ae7c-4cec-49c3-89ea-04e8c43261ff
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetIE5PasteMode
Sets the paste operation to be compatible with Microsoft Internet Explorer 5.  
  
## Syntax  
  
```  
  
      HRESULT SetIE5PasteMode(  
   bool bNewValue   
) const;  
```  
  
#### Parameters  
 `bNewValue`  
 If true, all paste operations are compatible with Internet Explorer 5; if false, paste operations are compatible with Internet Explorer 5.5.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM IE50_PASTE_MODE command ID](https://msdn.microsoft.com/en-us/library/aa769923.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::IE50Paste](../vs140/CHtmlEditCtrlBase--IE50Paste.md)