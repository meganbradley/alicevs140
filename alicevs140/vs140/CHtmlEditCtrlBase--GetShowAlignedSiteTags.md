---
title: "CHtmlEditCtrlBase::GetShowAlignedSiteTags"
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
ms.assetid: c93237b5-b72a-42c2-9ea9-71af368b2d6c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetShowAlignedSiteTags
Returns whether a glyph is displayed for all elements that have a **styleFloat** property.  
  
## Syntax  
  
```  
  
      HRESULT GetShowAlignedSiteTags(  
   bool& bCurValue   
) const;  
```  
  
#### Parameters  
 `bCurValue`  
 True if a glyph is displayed for all elements that have a **styleFloat** property; false if no glyph is displayed.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 For more information, see [IDM_SHOWALIGNEDSITETAGS Command ID](https://msdn.microsoft.com/en-us/library/aa769947.aspx).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetShowAlignedSiteTags](../vs140/CHtmlEditCtrlBase--SetShowAlignedSiteTags.md)