---
title: "CButton::SetButtonStyle"
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
ms.assetid: 422d4ef6-8368-4558-afbe-d1cf365da4ae
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetButtonStyle
Changes the style of a button.  
  
## Syntax  
  
```  
  
      void SetButtonStyle(  
   UINT nStyle,  
   BOOL bRedraw = TRUE   
);  
```  
  
#### Parameters  
 `nStyle`  
 Specifies the [button style](../vs140/Button-Styles.md).  
  
 `bRedraw`  
 Specifies whether the button is to be redrawn. A nonzero value redraws the button. A 0 value does not redraw the button. The button is redrawn by default.  
  
## Remarks  
 Use the `GetButtonStyle` member function to retrieve the button style. The low-order word of the complete button style is the button-specific style.  
  
## Example  
 [!CODE [NVC_MFC_CButton#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#5)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetButtonStyle](../vs140/CButton--GetButtonStyle.md)   
 [BM_SETSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb761824)