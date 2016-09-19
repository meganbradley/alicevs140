---
title: "CDocument::GetNextView"
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
ms.assetid: 8fea89b7-c652-4b99-a477-a1adb126e3c8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::GetNextView
Call this function to iterate through all of the document's views.  
  
## Syntax  
  
```  
  
      virtual CView* GetNextView(  
   POSITION& rPosition   
) const;  
```  
  
#### Parameters  
 `rPosition`  
 A reference to a **POSITION** value returned by a previous call to the `GetNextView` or [GetFirstViewPosition](../vs140/CDocument--GetFirstViewPosition.md) member functions. This value must not be **NULL**.  
  
## Return Value  
 A pointer to the view identified by `rPosition`.  
  
## Remarks  
 The function returns the view identified by `rPosition` and then sets `rPosition` to the **POSITION** value of the next view in the list. If the retrieved view is the last in the list, then `rPosition` is set to **NULL**.  
  
## Example  
 [!CODE [NVC_MFCDocView#59](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#59)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::AddView](../vs140/CDocument--AddView.md)   
 [CDocument::GetFirstViewPosition](../vs140/CDocument--GetFirstViewPosition.md)   
 [CDocument::RemoveView](../vs140/CDocument--RemoveView.md)   
 [CDocument::UpdateAllViews](../vs140/CDocument--UpdateAllViews.md)