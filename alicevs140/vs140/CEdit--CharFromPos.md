---
title: "CEdit::CharFromPos"
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
ms.assetid: 5353152b-c154-430e-814d-56f5d92d510f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::CharFromPos
Call this function to retrieve the zero-based line and character indices of the character nearest the specified point in this `CEdit` control  
  
## Syntax  
  
```  
  
      int CharFromPos(  
   CPoint pt   
) const;  
```  
  
#### Parameters  
 `pt`  
 The coordinates of a point in the client area of this `CEdit` object.  
  
## Return Value  
 The character index in the low-order **WORD**, and the line index in the high-order **WORD**.  
  
## Remarks  
  
> [!NOTE]
>  This member function is available beginning with Windows 95 and Windows NT 4.0.  
  
 For more information, see [EM_CHARFROMPOS](http://msdn.microsoft.com/library/windows/desktop/bb761566) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::PosFromChar](../vs140/CEdit--PosFromChar.md)