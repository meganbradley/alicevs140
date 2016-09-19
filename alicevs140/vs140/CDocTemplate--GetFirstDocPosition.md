---
title: "CDocTemplate::GetFirstDocPosition"
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
ms.assetid: f09ef3b5-8249-4cb9-9867-dab585b67c44
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::GetFirstDocPosition
Retrieves the position of the first document associated with this template.  
  
## Syntax  
  
```  
  
virtual POSITION GetFirstDocPosition( ) const = 0;  
  
```  
  
## Return Value  
 A **POSITION** value that can be used to iterate through the list of documents associated with this document template; or **NULL** if the list is empty.  
  
## Remarks  
 Use this function to get the position of the first document in the list of documents associated with this template. Use the **POSITION** value as an argument to [CDocTemplate::GetNextDoc](../vs140/CDocTemplate--GetNextDoc.md) to iterate through the list of documents associated with the template.  
  
 [CSingleDocTemplate](../vs140/CSingleDocTemplate-Class.md) and [CMultiDocTemplate](../vs140/CMultiDocTemplate-Class.md) both override this pure virtual function. Any class you derive from `CDocTemplate` must also override this function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate::GetNextDoc](../vs140/CDocTemplate--GetNextDoc.md)   
 [CSingleDocTemplate Class](../vs140/CSingleDocTemplate-Class.md)   
 [CMultiDocTemplate Class](../vs140/CMultiDocTemplate-Class.md)