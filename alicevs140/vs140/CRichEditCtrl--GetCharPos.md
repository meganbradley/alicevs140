---
title: "CRichEditCtrl::GetCharPos"
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
ms.assetid: 9d627e8e-6837-44d8-af53-7b3626c3f954
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetCharPos
Gets the position (top-left corner) of a given character within this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      CPoint GetCharPos(  
   long lChar   
) const;  
```  
  
#### Parameters  
 `lChar`  
 Zero-based index of the character.  
  
## Return Value  
 The location of the top-left corner of the character specified by `lChar`.  
  
## Remarks  
 The character is specified by giving its zero-based index value. If `lChar` is greater than the index of the last character in this `CRichEditCtrl` object, the return value specifies the coordinates of the character position just past the last character in this `CRichEditCtrl` object.  
  
 For more information, see [EM_POSFROMCHAR](http://msdn.microsoft.com/library/windows/desktop/bb761631) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::FindText](../vs140/CRichEditCtrl--FindText.md)