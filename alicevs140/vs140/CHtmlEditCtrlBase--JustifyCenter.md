---
title: "CHtmlEditCtrlBase::JustifyCenter"
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
ms.assetid: 323c4f82-f706-4a53-af26-cfe428f59501
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::JustifyCenter
Centers the format block in which the current selection is located.  
  
## Syntax  
  
```  
  
HRESULT JustifyCenter( ) const;  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_JUSTIFYCENTER command ID](https://msdn.microsoft.com/en-us/library/aa769989.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::JustifyLeft](../vs140/CHtmlEditCtrlBase--JustifyLeft.md)   
 [CHtmlEditCtrlBase::JustifyRight](../vs140/CHtmlEditCtrlBase--JustifyRight.md)