---
title: "CHtmlEditCtrlBase::GetShowStyleTags"
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
ms.assetid: e8bca133-ac6d-4d76-8764-928f2030eb2e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetShowStyleTags
Retrieves whether the WebBrowser displays a glyph for all the style tags.  
  
## Syntax  
  
```  
  
      HRESULT GetShowStyleTags(  
   bool& bCurValue   
) const;  
```  
  
#### Parameters  
 `bCurValue`  
 True if the WebBrowser displays a glyph for all the style tags, false if it does not  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 For more information, see [IDM_SHOWSTYLETAGS Command ID](https://msdn.microsoft.com/en-us/library/aa769954.aspx).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetShowStyleTags](../vs140/CHtmlEditCtrlBase--SetShowStyleTags.md)