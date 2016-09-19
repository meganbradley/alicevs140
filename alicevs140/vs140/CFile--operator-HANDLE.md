---
title: "CFile::operator HANDLE"
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
ms.assetid: 9a0d67a7-7cdd-4e3d-8042-c29275aa7ef7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::operator HANDLE
Use this operator to pass a handle to a `CFile` object to functions such as [ReadFileEx](http://msdn.microsoft.com/library/windows/desktop/aa365468) and [GetFileTime](http://msdn.microsoft.com/library/windows/desktop/ms724320) that expect a `HANDLE`.  
  
## Syntax  
  
```  
  
operator HANDLE( ) const;  
  
```  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::m_hFile](../vs140/CFile--m_hFile.md)