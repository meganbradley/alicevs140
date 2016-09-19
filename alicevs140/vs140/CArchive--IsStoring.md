---
title: "CArchive::IsStoring"
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
ms.assetid: 201bc713-6f91-40e2-9d34-ed6999b8484d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::IsStoring
Determines whether the archive is storing data.  
  
## Syntax  
  
```  
  
BOOL IsStoring( ) const;  
```  
  
## Return Value  
 Nonzero if the archive is currently being used for storing; otherwise 0.  
  
## Remarks  
 This member function is called by the `Serialize` functions of the archived classes.  
  
 If the `IsStoring` status of an archive is nonzero, then its `IsLoading` status is 0, and vice versa.  
  
## Example  
 [!CODE [NVC_MFCSerialization#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#17)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::IsLoading](../vs140/CArchive--IsLoading.md)