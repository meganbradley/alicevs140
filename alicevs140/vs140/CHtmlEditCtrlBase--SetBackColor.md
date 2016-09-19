---
title: "CHtmlEditCtrlBase::SetBackColor"
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
ms.assetid: efa30f4b-8989-43bc-a2ff-b40cc99a43f9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetBackColor
Sets the background color of the current selection.  
  
## Syntax  
  
```  
  
      HRESULT SetBackColor(  
   int nColor   
) const;  
HRESULT SetBackColor(  
   LPCTSTR szColor   
) const;  
```  
  
#### Parameters  
 `nColor`  
 The color. See `pvaIn` in [IDM_BACKCOLOR Command ID](https://msdn.microsoft.com/en-us/library/aa769858.aspx).  
  
 `szColor`  
 The color. See `pvaIn` in [IDM_BACKCOLOR Command ID](https://msdn.microsoft.com/en-us/library/aa769858.aspx).  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_BACKCOLOR_ command ID](https://msdn.microsoft.com/en-us/library/aa769858.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetBackColor](../vs140/CHtmlEditCtrlBase--GetBackColor.md)