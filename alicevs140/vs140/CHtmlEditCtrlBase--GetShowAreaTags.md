---
title: "CHtmlEditCtrlBase::GetShowAreaTags"
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
ms.assetid: 884859ac-bb9e-4a1e-a638-78e8b4377fe5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetShowAreaTags
Retrieves whether the WebBrowser displays a glyph for area tags.  
  
## Syntax  
  
```  
  
      HRESULT GetShowAreaTags(  
   bool& bCurValue   
) const;  
```  
  
#### Parameters  
 `bCurValue`  
 True if the WebBrowser displays a glyph for area tags, false if it does not.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 For more information, see [IDM_SHOWAREATAGS Command ID](https://msdn.microsoft.com/en-us/library/aa769949.aspx).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetShowAreaTags](../vs140/CHtmlEditCtrlBase--SetShowAreaTags.md)