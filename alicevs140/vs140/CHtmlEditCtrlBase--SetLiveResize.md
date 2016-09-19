---
title: "CHtmlEditCtrlBase::SetLiveResize"
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
ms.assetid: dfd5a64a-2ec9-4f99-a1f8-5e6e45505f19
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetLiveResize
Causes the WebBrowser to update an element's appearance continuously during a resizing or moving operation, rather than updating only at the completion of the move or resize.  
  
## Syntax  
  
```  
  
      HRESULT SetLiveResize(  
   bool bNewValue   
) const;  
```  
  
#### Parameters  
 `bNewValue`  
 If true, causes the WebBrowser to update an element's appearance continuously during a resizing or moving operation; if false, it updates only at the completion of the move or resize.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM LIVERESIZE command ID](https://msdn.microsoft.com/en-us/library/aa769928.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)