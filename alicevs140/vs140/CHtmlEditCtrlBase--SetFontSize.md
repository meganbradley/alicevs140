---
title: "CHtmlEditCtrlBase::SetFontSize"
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
ms.assetid: 0aa5d1dd-48df-4dee-a955-e84e9bde3479
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetFontSize
Sets the font size for the current selection.  
  
## Syntax  
  
```  
  
      HRESULT SetFontSize(  
   unsigned short size   
) const;  
```  
  
#### Parameters  
 `size`  
 The HTML font size (1-7). A value of 0 sets the font size to 1.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM FONTSIZE command ID](https://msdn.microsoft.com/en-us/library/aa769881.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetFontSize](../vs140/CHtmlEditCtrlBase--GetFontSize.md)   
 [CHtmlEditCtrlBase::GetFontFace](../vs140/CHtmlEditCtrlBase--GetFontFace.md)