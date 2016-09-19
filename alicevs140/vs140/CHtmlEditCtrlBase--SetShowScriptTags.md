---
title: "CHtmlEditCtrlBase::SetShowScriptTags"
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
ms.assetid: f922d272-abe4-4f33-bfe7-d8b84f1fa260
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetShowScriptTags
Displays a glyph for all the script tags.  
  
## Syntax  
  
```  
  
      HRESULT SetShowScriptTags(  
   bool bNewValue   
) const;  
```  
  
#### Parameters  
 `bNewValue`  
 If true, displays a glyph for all the script tags.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM SHOWSCRIPTTAGS command ID](https://msdn.microsoft.com/en-us/library/aa769953.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetShowScriptTags](../vs140/CHtmlEditCtrlBase--GetShowScriptTags.md)