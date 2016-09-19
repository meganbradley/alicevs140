---
title: "CColorDialog::GetColor"
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
ms.assetid: 57dcfbe3-7c5d-4837-86af-31aa19aef3b0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CColorDialog::GetColor
Call this function after calling `DoModal` to retrieve the information about the color the user selected.  
  
## Syntax  
  
```  
  
COLORREF GetColor( ) const;  
```  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value that contains the RGB information for the color selected in the color dialog box.  
  
## Example  
 [!CODE [NVC_MFCDocView#50](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#50)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CColorDialog Class](../vs140/CColorDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CColorDialog::SetCurrentColor](../vs140/CColorDialog--SetCurrentColor.md)