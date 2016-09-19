---
title: "CGopherFileFind::GetLength"
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
ms.assetid: 35fc7bf8-1285-44b4-9799-d811dfea2646
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherFileFind::GetLength
Call this member function to get the length, in bytes, of the found file.  
  
## Syntax  
  
```  
  
virtual ULONGLONG GetLength( ) const;  
  
```  
  
## Return Value  
 The length, in bytes, of the found file.  
  
## Remarks  
 `GetLength` uses the Win32 structure [WIN32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) to get the value of the file size in bytes.  
  
> [!NOTE]
>  As of MFC 7.0, `GetLength` supports 64-bit integer types. Previously-existing code built with this newer version of the library may result in truncation warnings.  
  
## Example  
 See the example for [CFile::GetLength](../vs140/CFile--GetLength.md) (the base class implementation).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CGopherFileFind Class](../vs140/CGopherFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileFind Class](../vs140/CFileFind-Class.md)