---
title: "CHtmlEditCtrlBase::JustifyRight"
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
ms.assetid: a067788d-06de-4655-a1a3-99cf71be2d82
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::JustifyRight
Right-justifies the format block in which the current selection is located.  
  
## Syntax  
  
```  
  
HRESULT JustifyRight( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_JUSTIFYRIGHT command ID](https://msdn.microsoft.com/en-us/library/aa770013.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::JustifyCenter](../vs140/CHtmlEditCtrlBase--JustifyCenter.md)   
 [CHtmlEditCtrlBase::JustifyLeft](../vs140/CHtmlEditCtrlBase--JustifyLeft.md)