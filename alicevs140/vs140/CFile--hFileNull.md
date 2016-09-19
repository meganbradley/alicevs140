---
title: "CFile::hFileNull"
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
ms.assetid: a12b872c-8cff-46f8-b1f7-2784ce0a027d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::hFileNull
Determines the presence of a valid file handle for the `CFile` object.  
  
## Syntax  
  
```  
  
static AFX_DATA const HANDLE hFileNull;  
  
```  
  
## Remarks  
 This constant is used to determine if the `CFile` object has a valid file handle.  
  
 The following example demonstrates this operation:  
  
 [!CODE [NVC_MFCFiles#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#22)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)