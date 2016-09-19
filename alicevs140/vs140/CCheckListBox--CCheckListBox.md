---
title: "CCheckListBox::CCheckListBox"
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
ms.assetid: 7ef3c30a-ddf0-40fc-a9d5-6e7c429d11a0
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCheckListBox::CCheckListBox
Constructs a `CCheckListBox` object.  
  
## Syntax  
  
```  
  
CCheckListBox( );  
  
```  
  
## Remarks  
 You construct a `CCheckListBox` object in two steps. First define a class derived from `CCheckListBox`, then call **Create**, which initializes the Windows checklist box and attaches it to the `CCheckListBox` object.  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#60](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#60)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCheckListBox Class](../vs140/CCheckListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCheckListBox::Create](../vs140/CCheckListBox--Create.md)