---
title: "CComboBox::Clear"
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
ms.assetid: dcd6f6ec-3303-4a29-a470-3dc00f961777
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::Clear
Deletes (clears) the current selection, if any, in the edit control of the combo box.  
  
## Syntax  
  
```  
  
void Clear( );  
```  
  
## Remarks  
 To delete the current selection and place the deleted contents onto the Clipboard, use the [Cut](../vs140/CComboBox--Cut.md) member function.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#4)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::Copy](../vs140/CComboBox--Copy.md)   
 [CComboBox::Cut](../vs140/CComboBox--Cut.md)   
 [CComboBox::Paste](../vs140/CComboBox--Paste.md)   
 [WM_CLEAR](http://msdn.microsoft.com/library/windows/desktop/ms649020)