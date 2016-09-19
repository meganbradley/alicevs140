---
title: "CRichEditCtrl::CharFromPos"
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
ms.assetid: 57686d42-fdd7-46d2-b76d-f66cdfd29111
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::CharFromPos
Retrieves information about the character at the point specified by the parameter `pt`.  
  
## Syntax  
  
```  
  
      int CharFromPos(  
   CPoint pt   
) const;  
```  
  
#### Parameters  
 `pt`  
 A [CPoint](../vs140/CPoint-Class.md) object containing the coordinates of the specified point.  
  
## Return Value  
 The zero-based character index of the character nearest the specified point. If the specified point is beyond the last character in the control, the return value indicates the last character in the control.  
  
## Remarks  
 This member function works with a rich edit control. To get the information for an edit control, call [CEdit::CharFromPos](../vs140/CEdit--CharFromPos.md).  
  
 For more information, see [EM_CHARFROMPOS](http://msdn.microsoft.com/library/windows/desktop/bb761566) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::PosFromChar](../vs140/CRichEditCtrl--PosFromChar.md)