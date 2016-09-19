---
title: "CHtmlEditCtrlBase::SetBookMark"
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
ms.assetid: dcf24221-47f7-42c7-ba35-b006f5f6ec5a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetBookMark
Creates a bookmark anchor for the current selection or insertion point.  
  
## Syntax  
  
```  
  
      HRESULT SetBookMark(  
   LPCTSTR szAnchorName   
) const;  
```  
  
#### Parameters  
 *szAnchorName*  
 The anchor name.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_BOOKMARK command ID](https://msdn.microsoft.com/en-us/library/aa769873.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetBookMark](../vs140/CHtmlEditCtrlBase--GetBookMark.md)   
 [CHtmlEditCtrlBase::UnBookmark](../vs140/CHtmlEditCtrlBase--UnBookmark.md)