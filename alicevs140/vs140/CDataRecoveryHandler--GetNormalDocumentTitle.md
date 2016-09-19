---
title: "CDataRecoveryHandler::GetNormalDocumentTitle"
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
ms.assetid: 1a876830-605a-43c0-b1e1-4bf5d1096dd3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::GetNormalDocumentTitle
Retrieves the normal title for the specified document.  
  
## Syntax  
  
```  
virtual CString GetNormalDocumentTitle(  
   CDocument *pDocument  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pDocument`|A pointer to a `CDocument`.|  
  
## Return Value  
 The normal title for the specified document.  
  
## Remarks  
 The normal title of a document is usually the file name of the document without the path. This is the title in the **File name** field of the **Save As** dialog box.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)