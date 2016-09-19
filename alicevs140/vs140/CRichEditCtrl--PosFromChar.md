---
title: "CRichEditCtrl::PosFromChar"
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
ms.assetid: 24e32ab7-fafd-4299-a035-daf279a437e9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::PosFromChar
Retrieves the client area coordinates of a specified character in an edit control.  
  
## Syntax  
  
```  
  
      CPoint PosFromChar(  
   UINT nChar   
) const;  
```  
  
#### Parameters  
 `nChar`  
 The zero-based index of the character.  
  
## Return Value  
 The position of the character, (x, y). For a single-line edit control, the y-coordinate is always zero.  
  
## Remarks  
 For more information, see [EM_POSFROMCHAR](http://msdn.microsoft.com/library/windows/desktop/bb761631) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetCharPos](../vs140/CRichEditCtrl--GetCharPos.md)