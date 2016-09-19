---
title: "CFileFind::Close"
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
ms.assetid: add4ec7c-90b8-49ee-9743-b1ae8f439f5b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::Close
Call this member function to end the search, reset the context, and release all resources.  
  
## Syntax  
  
```  
  
void Close( );  
  
```  
  
## Remarks  
 After calling **Close**, you do not have to create a new `CFileFind` instance before calling [FindFile](../vs140/CFileFind--FindFile.md) to begin a new search.  
  
## Example  
 See the example for [CFileFind::GetFileName](../vs140/CFileFind--GetFileName.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)