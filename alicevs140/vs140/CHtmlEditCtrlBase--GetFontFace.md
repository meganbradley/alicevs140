---
title: "CHtmlEditCtrlBase::GetFontFace"
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
ms.assetid: 47e14efa-fb55-4171-a7aa-40ac2c94aeeb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetFontFace
Retrieves the font name for the current selection.  
  
## Syntax  
  
```  
  
      HRESULT GetFontFace(  
   CString& strFace   
) const;  
```  
  
#### Parameters  
 `strFace`  
 The font name.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 If the current selection uses more than one font, `strFace` will be an empty string.  
  
 This method sends the [IDM_FONTNAME command ID](https://msdn.microsoft.com/en-us/library/aa769880.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetFontFace](../vs140/CHtmlEditCtrlBase--SetFontFace.md)   
 [CHtmlEditCtrlBase::GetFontSize](../vs140/CHtmlEditCtrlBase--GetFontSize.md)