---
title: "CButton::GetTextMargin"
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
ms.assetid: b3d27e6c-b9c0-47d2-96df-97d91499b9f6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetTextMargin
Call this method to get the text margin of the `CButton` object.  
  
## Syntax  
  
```  
  
      BOOL GetTextMargin(  
   RECT* pmargin   
);  
```  
  
#### Parameters  
 `pmargin`  
 A pointer to the text margin of the `CButton` object.  
  
## Return Value  
 Returns the text margin.  
  
## Remarks  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function emulates the functionality of the **BCM_GETTEXTMARGIN** message, as described in the [Buttons](http://msdn.microsoft.com/library/windows/desktop/bb775943) section of the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [CButton::SetTextMargin](../vs140/CButton--SetTextMargin.md)