---
title: "CDocument::IsModified"
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
ms.assetid: 048ea368-69a0-4fe4-917a-530ae3c110ae
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::IsModified
Call this function to determine whether the document has been modified since it was last saved.  
  
## Syntax  
  
```  
  
virtual BOOL IsModified( );  
```  
  
## Return Value  
 Nonzero if the document has been modified since it was last saved; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::SetModifiedFlag](../vs140/CDocument--SetModifiedFlag.md)   
 [CDocument::SaveModified](../vs140/CDocument--SaveModified.md)