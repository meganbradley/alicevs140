---
title: "CEdit::GetRect"
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
ms.assetid: 00d66450-9654-4df5-ab54-308db53b72cd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::GetRect
Call this function to get the formatting rectangle of an edit control.  
  
## Syntax  
  
```  
  
      void GetRect(  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `lpRect`  
 Points to the `RECT` structure that receives the formatting rectangle.  
  
## Remarks  
 The formatting rectangle is the limiting rectangle of the text, which is independent of the size of the edit-control window.  
  
 The formatting rectangle of a multiple-line edit control can be modified by the [SetRect](../vs140/CEdit--SetRect.md) and [SetRectNP](../vs140/CEdit--SetRectNP.md) member functions.  
  
 For more information, see [EM_GETRECT](http://msdn.microsoft.com/library/windows/desktop/bb761596) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEdit::LimitText](../vs140/CEdit--LimitText.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::SetRect](../vs140/CEdit--SetRect.md)   
 [CEdit::SetRectNP](../vs140/CEdit--SetRectNP.md)