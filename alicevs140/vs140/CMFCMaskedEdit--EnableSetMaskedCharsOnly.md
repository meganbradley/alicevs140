---
title: "CMFCMaskedEdit::EnableSetMaskedCharsOnly"
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
ms.assetid: 5cfdb7ec-08a9-41f3-afef-df7144214413
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMaskedEdit::EnableSetMaskedCharsOnly
Specifies whether the text is validated against only the masked characters, or against the whole mask.  
  
## Syntax  
  
```  
void EnableSetMaskedCharsOnly(  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to validate the user input against only masked characters; `FALSE` to validate against the whole mask. The default value is `TRUE`.  
  
## Requirements  
 **Header:** afxmaskededit.h  
  
## See Also  
 [CMFCMaskedEdit Class](../vs140/CMFCMaskedEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)