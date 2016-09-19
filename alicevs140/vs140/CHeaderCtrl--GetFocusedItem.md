---
title: "CHeaderCtrl::GetFocusedItem"
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
ms.assetid: e6906306-48e8-462e-b207-95f8bc4da5c5
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::GetFocusedItem
Gets the index of the item that has the focus in the current header control.  
  
## Syntax  
  
```  
int GetFocusedItem() const;  
```  
  
## Return Value  
 The zero-based index of the header item that has the focus.  
  
## Remarks  
 This method sends the [HDM_GETFOCUSEDITEM](http://msdn.microsoft.com/library/windows/desktop/bb775330) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_headerCtrl`, that is used to access the current header control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CHeaderCtrl_s4#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl_s4#6)]  
  
## Example  
 The following code example demonstrates the `SetFocusedItem` and `GetFocusedItem` methods. In an earlier section of the code, we created a header control with five columns. However, you can drag a column separator so that the column is not visible. The following example sets and then confirms the last column header as the focus item.  
  
 [!CODE [NVC_MFC_CHeaderCtrl_s4#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl_s4#4)]  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [HDM_GETFOCUSEDITEM](http://msdn.microsoft.com/library/windows/desktop/bb775330)   
 [CHeaderCtrl::SetFocusedItem](../vs140/CHeaderCtrl--SetFocusedItem.md)