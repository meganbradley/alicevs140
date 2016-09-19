---
title: "CTaskDialog::OnHyperlinkClick"
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
ms.assetid: e4d47495-c136-41ad-ac9b-a52389001d0a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::OnHyperlinkClick
The framework calls this method when the user clicks on a hyperlink.  
  
## Syntax  
  
```  
virtual HRESULT OnHyperlinkClick(  
   const CString& strHref  
);  
```  
  
#### Parameters  
 [in] `strHref`  
 The string that represents the hyperlink.  
  
## Return Value  
 The default implementation returns `S_OK`.  
  
## Remarks  
 This method calls [ShellExecute](http://msdn.microsoft.com/library/windows/desktop/bb762153) before it returns `S_OK`.  
  
 Override this method in a derived class to implement custom behavior.  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::TaskDialogCallback](../vs140/CTaskDialog--TaskDialogCallback.md)