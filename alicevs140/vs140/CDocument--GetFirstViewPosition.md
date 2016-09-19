---
title: "CDocument::GetFirstViewPosition"
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
ms.assetid: 960181d5-1c5c-4335-b19d-ad259faa9a68
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::GetFirstViewPosition
Call this function to get the position of the first view in the list of views associated with the document.  
  
## Syntax  
  
```  
  
virtual POSITION GetFirstViewPosition( ) const;  
```  
  
## Return Value  
 A **POSITION** value that can be used for iteration with the [GetNextView](../vs140/CDocument--GetNextView.md) member function.  
  
## Example  
 [!CODE [NVC_MFCDocView#59](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#59)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::GetNextView](../vs140/CDocument--GetNextView.md)