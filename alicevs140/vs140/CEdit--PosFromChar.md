---
title: "CEdit::PosFromChar"
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
ms.assetid: 38763d66-3e04-4085-806f-0d78ef32ffa2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::PosFromChar
Call this function to get the position (top-left corner) of a given character within this `CEdit` object.  
  
## Syntax  
  
```  
  
      CPoint PosFromChar(  
   UINT nChar   
) const;  
```  
  
#### Parameters  
 `nChar`  
 The zero-based index of the specified character.  
  
## Return Value  
 The coordinates of the top-left corner of the character specified by `nChar`.  
  
## Remarks  
 The character is specified by giving its zero-based index value. If `nChar` is greater than the index of the last character in this `CEdit` object, the return value specifies the coordinates of the character position just past the last character in this `CEdit` object.  
  
> [!NOTE]
>  This member function is available beginning with Windows 95 and Windows NT 4.0.  
  
 For more information, see [EM_POSFROMCHAR](http://msdn.microsoft.com/library/windows/desktop/bb761631) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEdit::LineFromChar](../vs140/CEdit--LineFromChar.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::CharFromPos](../vs140/CEdit--CharFromPos.md)