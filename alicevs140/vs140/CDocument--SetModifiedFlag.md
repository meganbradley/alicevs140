---
title: "CDocument::SetModifiedFlag"
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
ms.assetid: c9b06b79-c4d6-4cb8-a52a-b7b12c936f53
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::SetModifiedFlag
Call this function after you have made any modifications to the document.  
  
## Syntax  
  
```  
  
      virtual void SetModifiedFlag(  
   BOOL bModified = TRUE   
);  
```  
  
#### Parameters  
 `bModified`  
 Flag indicating whether the document has been modified.  
  
## Remarks  
 By calling this function consistently, you ensure that the framework prompts the user to save changes before closing a document. Typically you should use the default value of **TRUE** for the `bModified` parameter. To mark a document as clean (unmodified), call this function with a value of **FALSE**.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::IsModified](../vs140/CDocument--IsModified.md)   
 [CDocument::SaveModified](../vs140/CDocument--SaveModified.md)