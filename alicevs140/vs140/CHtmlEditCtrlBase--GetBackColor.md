---
title: "CHtmlEditCtrlBase::GetBackColor"
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
ms.assetid: fa5484df-777a-4a74-affe-57ee320815cf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetBackColor
Retrieves the background color of the current selection.  
  
## Syntax  
  
```  
  
      HRESULT GetBackColor(  
   int& nColor   
) const;  
```  
  
#### Parameters  
 `nColor`  
 The background color.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_BACKCOLOR Command ID](https://msdn.microsoft.com/en-us/library/aa769858.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetBackColor](../vs140/CHtmlEditCtrlBase--SetBackColor.md)   
 [CHtmlEditCtrlBase::GetForeColor](../vs140/CHtmlEditCtrlBase--GetForeColor.md)