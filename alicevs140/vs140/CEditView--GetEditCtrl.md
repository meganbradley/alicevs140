---
title: "CEditView::GetEditCtrl"
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
ms.assetid: 72169fc2-7207-4023-908b-366faebede3f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::GetEditCtrl
Call `GetEditCtrl` to get a reference to the edit control used by the edit view.  
  
## Syntax  
  
```  
  
CEdit& GetEditCtrl( ) const;  
```  
  
## Return Value  
 A reference to a `CEdit` object.  
  
## Remarks  
 This control is of type [CEdit](../vs140/CEdit-Class.md), so you can manipulate the Windows edit control directly using the `CEdit` member functions.  
  
> [!CAUTION]
>  Using the `CEdit` object can change the state of the underlying Windows edit control. For example, you should not change the tab settings using the [CEdit::SetTabStops](../vs140/CEdit--SetTabStops.md) function because `CEditView` caches these settings for use both in the edit control and in printing. Instead, use [CEditView::SetTabStops](../vs140/CEditView--SetTabStops.md).  
  
## Example  
 [!CODE [NVC_MFCDocView#66](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#66)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit Class](../vs140/CEdit-Class.md)   
 [CEditView::SetTabStops](../vs140/CEditView--SetTabStops.md)