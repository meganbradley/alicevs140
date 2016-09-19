---
title: "CDatabase::CDatabase"
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
ms.assetid: 1491c94b-2cff-4133-b201-17e9b199e608
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::CDatabase
Constructs a `CDatabase` object.  
  
## Syntax  
  
```  
  
CDatabase( );  
```  
  
## Remarks  
 After constructing the object, you must call its `OpenEx` or **Open** member function to establish a connection to a specified data source.  
  
 You may find it convenient to embed the `CDatabase` object in your document class.  
  
## Example  
 This example illustrates using `CDatabase` in a `CDocument`-derived class.  
  
 [!CODE [NVC_MFCDatabase#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#9)]  
  
 [!CODE [NVC_MFCDatabase#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#10)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::OpenEx](../vs140/CDatabase--OpenEx.md)   
 [CDatabase::Open](../vs140/CDatabase--Open.md)