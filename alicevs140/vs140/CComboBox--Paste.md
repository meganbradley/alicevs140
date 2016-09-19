---
title: "CComboBox::Paste"
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
ms.assetid: cfe35b59-d8e2-47bb-8cc7-9b0e21d951c2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::Paste
Inserts the data from the Clipboard into the edit control of the combo box at the current cursor position.  
  
## Syntax  
  
```  
  
void Paste( );  
```  
  
## Remarks  
 Data is inserted only if the Clipboard contains data in **CF_TEXT** format.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#30](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#30)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::Clear](../vs140/CComboBox--Clear.md)   
 [CComboBox::Copy](../vs140/CComboBox--Copy.md)   
 [CComboBox::Cut](../vs140/CComboBox--Cut.md)   
 [WM_PASTE](http://msdn.microsoft.com/library/windows/desktop/ms649028)