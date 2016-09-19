---
title: "CMFCMaskedEdit::EnableGetMaskedCharsOnly"
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
ms.assetid: 9e72c126-3dca-47ea-a410-8a8c71e1912a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMaskedEdit::EnableGetMaskedCharsOnly
Specifies whether the `GetWindowText` method retrieves only masked characters.  
  
## Syntax  
  
```  
void EnableGetMaskedCharsOnly(  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to specify that the [CMFCMaskedEdit::GetWindowText](../vs140/CMFCMaskedEdit--GetWindowText.md) method retrieve only masked characters; `FALSE` to specify that the method retrieve the whole text. The default value is `TRUE`.  
  
## Remarks  
 Use this method to enable retrieving masked characters. Then create a masked edit control that corresponds to the telephone number, such as (425) 555-0187. If you call the `GetWindowText` method, it returns "4255550187". If you disable retrieving masked characters, the `GetWindowText` method returns the text that is displayed in the edit control, for example "(425) 555-0187".  
  
## Requirements  
 **Header:** afxmaskededit.h  
  
## See Also  
 [CMFCMaskedEdit Class](../vs140/CMFCMaskedEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)