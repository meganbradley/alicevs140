---
title: "CHtmlEditCtrlBase::GetFontSize"
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
ms.assetid: 5ec27253-3609-45af-9d30-2769c4d78cd1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetFontSize
Retrieves the font size for the current selection.  
  
## Syntax  
  
```  
  
      HRESULT GetFontSize(  
   short& nSize   
) const;  
```  
  
#### Parameters  
 `nSize`  
 The font size.  
  
## Return Value  
 Returns the HTML font size (1-7). Returns 0 if the selection contains multiple font sizes.  
  
## Remarks  
 This method sends the [IDM_FONTSIZE command ID](https://msdn.microsoft.com/en-us/library/aa769881.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetFontSize](../vs140/CHtmlEditCtrlBase--SetFontSize.md)   
 [CHtmlEditCtrlBase::GetFontFace](../vs140/CHtmlEditCtrlBase--GetFontFace.md)