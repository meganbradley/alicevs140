---
title: "CListBox::CListBox"
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
ms.assetid: 41d786e1-fbe1-4a5a-a013-e6cb337172b7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::CListBox
Constructs a `CListBox` object.  
  
## Syntax  
  
```  
  
CListBox( );  
```  
  
## Remarks  
 You construct a `CListBox` object in two steps. First, call the constructor **ClistBox** and then call **Create**, which initializes the Windows list box and attaches it to the `CListBox`.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#1)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::Create](../vs140/CListBox--Create.md)