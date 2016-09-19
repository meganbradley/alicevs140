---
title: "CDocument::GetPathName"
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
ms.assetid: da18fa41-21e6-48c0-bd2c-fbfee55dd991
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::GetPathName
Call this function to get the fully qualified path of the document's disk file.  
  
## Syntax  
  
```  
  
const CString& GetPathName( ) const;  
```  
  
## Return Value  
 The document's fully qualified path. This string is empty if the document has not been saved or does not have a disk file associated with it.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::SetPathName](../vs140/CDocument--SetPathName.md)