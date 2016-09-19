---
title: "CMDIChildWndEx::IsReadOnly"
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
ms.assetid: 99473388-a70d-4687-b78e-b8f27adfbf48
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::IsReadOnly
Specifies whether the document that is displayed in the child window is read-only.  
  
## Syntax  
  
```  
virtual BOOL IsReadOnly();  
```  
  
## Return Value  
 `TRUE` if the document is read-only; otherwise `FALSE`.  
  
## Remarks  
 This function is used to prevent saving of read-only documents.  
  
## Example  
 The following example demonstrates overriding the `IsReadOnly` method. This code snippet comes from the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#2](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#2)]  
  
## Requirements  
 **Header:** afxMDIChildWndEx.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)