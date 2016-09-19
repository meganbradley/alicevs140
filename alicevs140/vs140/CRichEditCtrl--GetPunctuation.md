---
title: "CRichEditCtrl::GetPunctuation"
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
ms.assetid: 951840fd-fe7b-441b-90cc-95c3483c4d24
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetPunctuation
Gets the current punctuation characters in a rich edit control.  
  
## Syntax  
  
```  
  
      BOOL GetPunctuation(  
   UINT fType,  
   PUNCTUATION* lpPunc   
) const;  
```  
  
#### Parameters  
 `fType`  
 The punctuation type flag, as described in the `fType` parameter of [EM_GETPUNCTUATION](http://msdn.microsoft.com/library/windows/desktop/bb774184) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `lpPunc`  
 A pointer to a [PUNCTUATION](http://msdn.microsoft.com/library/windows/desktop/bb787944) structure, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if the operation succeeded, otherwise 0.  
  
## Remarks  
 This member function is available with only the Asian-language versions of the operating system.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::SetPunctuation](../vs140/CRichEditCtrl--SetPunctuation.md)