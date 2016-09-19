---
title: "CDocTemplate::AddDocument"
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
ms.assetid: d72727dd-7101-4a38-bb25-b00f7bec637e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::AddDocument
Use this function to add a document to a template.  
  
## Syntax  
  
```  
  
      virtual void AddDocument(  
   CDocument* pDoc   
);  
```  
  
#### Parameters  
 `pDoc`  
 A pointer to the document to be added.  
  
## Remarks  
 The derived classes [CMultiDocTemplate](../vs140/CMultiDocTemplate-Class.md) and [CSingleDocTemplate](../vs140/CSingleDocTemplate-Class.md) override this function. If you derive your own document-template class from `CDocTemplate`, your derived class must override this function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate::RemoveDocument](../vs140/CDocTemplate--RemoveDocument.md)   
 [CMultiDocTemplate Class](../vs140/CMultiDocTemplate-Class.md)   
 [CSingleDocTemplate Class](../vs140/CSingleDocTemplate-Class.md)