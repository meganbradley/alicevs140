---
title: "CDocument::GetDocTemplate"
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
ms.assetid: a02c4f2e-8800-4a40-bd2d-85ab64c0087c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::GetDocTemplate
Call this function to get a pointer to the document template for this document type.  
  
## Syntax  
  
```  
  
CDocTemplate* GetDocTemplate( ) const;  
```  
  
## Return Value  
 A pointer to the document template for this document type, or **NULL** if the document is not managed by a document template.  
  
## Example  
 [!CODE [NVC_MFCDocView#58](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#58)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)