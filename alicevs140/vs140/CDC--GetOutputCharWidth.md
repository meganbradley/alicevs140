---
title: "CDC::GetOutputCharWidth"
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
ms.assetid: 2b5c67de-6e96-4658-91aa-15defd8737b2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetOutputCharWidth
Uses the output device context, `m_hDC`, and retrieves the widths of individual characters in a consecutive group of characters from the current font.  
  
## Syntax  
  
```  
  
      BOOL GetOutputCharWidth(  
   UINT nFirstChar,  
   UINT nLastChar,  
   LPINT lpBuffer   
) const;  
```  
  
#### Parameters  
 `nFirstChar`  
 Specifies the first character in a consecutive group of characters in the current font.  
  
 `nLastChar`  
 Specifies the last character in a consecutive group of characters in the current font.  
  
 `lpBuffer`  
 Points to a buffer that will receive the width values for a consecutive group of characters in the current font.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 For example, if `nFirstChar` identifies the letter 'a' and `nLastChar` identifies the letter 'z', the function retrieves the widths of all lowercase characters.  
  
 The function stores the values in the buffer pointed to by `lpBuffer`. This buffer must be large enough to hold all of the widths; that is, there must be at least 26 entries in the example given.  
  
 If a character in the consecutive group of characters does not exist in a particular font, it will be assigned the width value of the default character.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetCharWidth](../vs140/CDC--GetCharWidth.md)   
 [CDC::m_hAttribDC](../vs140/CDC--m_hAttribDC.md)   
 [CDC::m_hDC](../vs140/CDC--m_hDC.md)   
 [GetCharWidth](http://msdn.microsoft.com/library/windows/desktop/dd144861)