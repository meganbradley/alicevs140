---
title: "CHtmlEditCtrlBase::GetForeColor"
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
ms.assetid: 25de685c-5f56-4382-a990-abaded607de9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetForeColor
Retrieves the foreground (text) color of the current selection.  
  
## Syntax  
  
```  
  
      HRESULT GetForeColor(  
   int & nColor   
);  
```  
  
#### Parameters  
 `nColor`  
 The foreground color.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_FORECOLOR Command ID](https://msdn.microsoft.com/en-us/library/aa769882.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetForeColor](../vs140/CHtmlEditCtrlBase--SetForeColor.md)   
 [CHtmlEditCtrlBase::GetBackColor](../vs140/CHtmlEditCtrlBase--GetBackColor.md)