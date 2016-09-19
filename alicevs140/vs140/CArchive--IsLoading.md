---
title: "CArchive::IsLoading"
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
ms.assetid: 837cd522-f78a-424e-9543-ee961edbfd5e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::IsLoading
Determines whether the archive is loading data.  
  
## Syntax  
  
```  
  
BOOL IsLoading( ) const;  
```  
  
## Return Value  
 Nonzero if the archive is currently being used for loading; otherwise 0.  
  
## Remarks  
 This member function is called by the `Serialize` functions of the archived classes.  
  
## Example  
 [!CODE [NVC_MFCSerialization#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#16)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::IsStoring](../vs140/CArchive--IsStoring.md)