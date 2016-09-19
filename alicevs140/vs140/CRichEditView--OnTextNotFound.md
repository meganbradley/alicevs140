---
title: "CRichEditView::OnTextNotFound"
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
ms.assetid: 696b8afe-698b-499e-a5b2-0ee4b63666cd
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnTextNotFound
Called by the framework whenever a search fails.  
  
## Syntax  
  
```  
  
      virtual void OnTextNotFound(  
   LPCTSTR lpszFind   
);  
```  
  
#### Parameters  
 `lpszFind`  
 The text which was not found.  
  
## Remarks  
 Override this function to change the output notification from a [MessageBeep](http://msdn.microsoft.com/library/windows/desktop/ms680356).  
  
 For more information, see [MessageBeep](http://msdn.microsoft.com/library/windows/desktop/ms680356) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#157](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#157)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::FindText](../vs140/CRichEditView--FindText.md)   
 [CRichEditView::FindTextSimple](../vs140/CRichEditView--FindTextSimple.md)   
 [CRichEditView::OnFindNext](../vs140/CRichEditView--OnFindNext.md)