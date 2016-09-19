---
title: "CDocTemplate::GetNextDoc"
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
ms.assetid: 1fcb977a-d3d5-4fcb-b138-f34c4c03408b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::GetNextDoc
Retrieves the list element identified by `rPos`, then sets `rPos` to the **POSITION** value of the next entry in the list.  
  
## Syntax  
  
```  
  
      virtual CDocument* GetNextDoc(  
   POSITION& rPos   
) const = 0;  
```  
  
## Return Value  
 A pointer to the next document in the list of documents associated with this template.  
  
#### Parameters  
 `rPos`  
 A reference to a **POSITION** value returned by a previous call to [GetFirstDocPosition](../vs140/CDocTemplate--GetFirstDocPosition.md) or `GetNextDoc`.  
  
## Remarks  
 If the retrieved element is the last in the list, then the new value of `rPos` is set to **NULL**.  
  
 You can use `GetNextDoc` in a forward iteration loop if you establish the initial position with a call to [GetFirstDocPosition](../vs140/CDocTemplate--GetFirstDocPosition.md).  
  
 You must ensure that your **POSITION** value represents a valid position in the list. If it is invalid, then the Debug version of the Microsoft Foundation Class Library asserts.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate::GetFirstDocPosition](../vs140/CDocTemplate--GetFirstDocPosition.md)