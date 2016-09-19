---
title: "CComboBox::Cut"
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
ms.assetid: 92895914-bf87-4731-9f6e-08b7c83e4109
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::Cut
Deletes (cuts) the current selection, if any, in the combo-box edit control and copies the deleted text onto the Clipboard in **CF_TEXT** format.  
  
## Syntax  
  
```  
  
void Cut( );  
```  
  
## Remarks  
 To delete the current selection without placing the deleted text onto the Clipboard, call the [Clear](../vs140/CComboBox--Clear.md) member function.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#7)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::Clear](../vs140/CComboBox--Clear.md)   
 [CComboBox::Copy](../vs140/CComboBox--Copy.md)   
 [CComboBox::Paste](../vs140/CComboBox--Paste.md)   
 [WM_CUT](http://msdn.microsoft.com/library/windows/desktop/ms649023)