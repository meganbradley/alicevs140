---
title: "CHtmlEditCtrlBase::JustifyLeft"
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
ms.assetid: dfca493c-dd82-4695-980e-1bbee46f4c0f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::JustifyLeft
Left-justifies the format block in which the current selection is located.  
  
## Syntax  
  
```  
  
HRESULT JustifyLeft( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_JUSTIFYLEFT command ID](https://msdn.microsoft.com/en-us/library/aa770011.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::JustifyCenter](../vs140/CHtmlEditCtrlBase--JustifyCenter.md)   
 [CHtmlEditCtrlBase::JustifyRight](../vs140/CHtmlEditCtrlBase--JustifyRight.md)