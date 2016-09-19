---
title: "CHtmlEditCtrlBase::Cut"
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
ms.assetid: 08f32bc3-beb5-4251-9c8e-15549dea9722
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::Cut
Copies the current selection to the clipboard and then deletes it.  
  
## Syntax  
  
```  
  
HRESULT Cut( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_CUT command ID](https://msdn.microsoft.com/en-us/library/aa769875.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::Delete](../vs140/CHtmlEditCtrlBase--Delete.md)   
 [CHtmlEditCtrlBase::Copy](../vs140/CHtmlEditCtrlBase--Copy.md)   
 [CHtmlEditCtrlBase::Paste](../vs140/CHtmlEditCtrlBase--Paste.md)