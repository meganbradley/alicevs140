---
title: "CHtmlEditCtrlBase::SetShowUnknownTags"
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
ms.assetid: 096afa0a-ec3f-4dee-93b5-aa4d97481a74
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetShowUnknownTags
Displays a glyph for all the unknown tags.  
  
## Syntax  
  
```  
  
      HRESULT SetShowUnknownTags(  
   bool bNewValue   
) const;  
```  
  
#### Parameters  
 `bNewValue`  
 If true, displays a glyph for all the unknown tags.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM SHOWUNKNOWNTAGS command ID](https://msdn.microsoft.com/en-us/library/aa769955.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetShowUnknownTags](../vs140/CHtmlEditCtrlBase--GetShowUnknownTags.md)