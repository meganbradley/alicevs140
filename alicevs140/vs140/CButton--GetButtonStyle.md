---
title: "CButton::GetButtonStyle"
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
ms.assetid: ba0ec0b8-5da7-4403-9e51-8da10a71a2db
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetButtonStyle
Retrieves information about the button control style.  
  
## Syntax  
  
```  
  
UINT GetButtonStyle( ) const;  
```  
  
## Return Value  
 Returns the button styles for this `CButton` object. This function returns only the [BS_](../vs140/Button-Styles.md) style values, not any of the other window styles.  
  
## Example  
 [!CODE [NVC_MFC_CButton#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#5)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::SetButtonStyle](../vs140/CButton--SetButtonStyle.md)   
 [GetWindowLong](http://msdn.microsoft.com/library/windows/desktop/ms633584)