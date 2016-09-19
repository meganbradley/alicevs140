---
title: "CButton::SetTextMargin"
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
ms.assetid: f05a3c08-a0d1-485a-b885-cad553ebec58
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetTextMargin
Call this method to set the text margin of the `CButton` object.  
  
## Syntax  
  
```  
  
      BOOL SetTextMargin(  
   RECT* pmargin  
);  
```  
  
#### Parameters  
 `pmargin`  
 A pointer to the new text margin.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Remarks  
 This member function emulates the functionality of the **BCM_SETTEXTMARGIN** message, as described in the [Buttons](http://msdn.microsoft.com/library/windows/desktop/bb775943) section of the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [CButton::GetTextMargin](../vs140/CButton--GetTextMargin.md)