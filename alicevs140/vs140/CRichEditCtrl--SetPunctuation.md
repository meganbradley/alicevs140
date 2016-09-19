---
title: "CRichEditCtrl::SetPunctuation"
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
ms.assetid: f8ff1547-06e0-452a-8a9c-49f030f73548
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetPunctuation
Sets the punctuation in a rich edit control.  
  
## Syntax  
  
```  
  
      BOOL SetPunctuation(  
   UINT fType,  
   PUNCTUATION* lpPunc   
);  
```  
  
#### Parameters  
 `fType`  
 The punctuation flag. For a list of possible values, see the `fType` parameter for [EM_SETPUNCTUATION](http://msdn.microsoft.com/library/windows/desktop/bb774278) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `lpPunc`  
 A pointer to a [PUNCTUATION](http://msdn.microsoft.com/library/windows/desktop/bb787944) structure, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if successful, otherwise 0.  
  
## Remarks  
 This member function is available for only Asian-language versions of the operating system.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetPunctuation](../vs140/CRichEditCtrl--GetPunctuation.md)