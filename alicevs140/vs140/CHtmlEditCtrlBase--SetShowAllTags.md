---
title: "CHtmlEditCtrlBase::SetShowAllTags"
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
ms.assetid: 3fe518be-b06b-4c97-9bcc-cf365ca5f1f1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetShowAllTags
Displays glyphs to show the location of all tags in a document.  
  
## Syntax  
  
```  
  
      HRESULT SetShowAllTags(  
   bool bNewValue   
) const;  
```  
  
#### Parameters  
 `bNewValue`  
 If true, displays glyphs to show the location of all tags in a document.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM SHOWALLTAGS command ID](https://msdn.microsoft.com/en-us/library/aa769948.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetShowAllTags](../vs140/CHtmlEditCtrlBase--GetShowAllTags.md)