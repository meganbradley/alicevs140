---
title: "CTaskDialog::DoModal"
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
ms.assetid: 397dcad6-305e-4341-84b9-356091d301be
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::DoModal
Shows the `CTaskDialog` and makes it modal.  
  
## Syntax  
  
```  
INT_PTR DoModal (  
   HWND hParent = ::GetActiveWindow()  
);  
```  
  
#### Parameters  
 [in] `hParent`  
 The parent window for the `CTaskDialog`.  
  
## Return Value  
 An integer that corresponds to the selection made by the user.  
  
## Remarks  
 Displays this instance of the [CTaskDialog](../vs140/CTaskDialog-Class.md). The application then waits for the user to close the dialog box.  
  
 The `CTaskDialog` closes when the user selects a common button, a command link control, or closes the `CTaskDialog`. The return value is the identifier that indicates how the user closed the dialog box.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#7)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)