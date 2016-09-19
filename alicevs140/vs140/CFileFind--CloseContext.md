---
title: "CFileFind::CloseContext"
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
ms.assetid: 66b40c92-0775-4e60-979c-6627ebb9b988
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::CloseContext
Closes the file specified by the current search handle.  
  
## Syntax  
  
```  
  
virtual void CloseContext( );  
  
```  
  
## Remarks  
 Closes the file specified by the current value of the search handle. Override this function to change the default behavior.  
  
 You must call the [FindFile](../vs140/CFileFind--FindFile.md) or [FindNextFile](../vs140/CFileFind--FindNextFile.md) functions at least once to retrieve a valid search handle. The **FindFile** and `FindNextFile` functions use the search handle to locate files with names that match a given name.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileFind::FindNextFile](../vs140/CFileFind--FindNextFile.md)   
 [CFileFind::FindFile](../vs140/CFileFind--FindFile.md)