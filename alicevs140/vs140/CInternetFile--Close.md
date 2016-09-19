---
title: "CInternetFile::Close"
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
ms.assetid: b1f1b23a-71fe-4274-9ceb-5fb2f3d74261
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetFile::Close
Closes a `CInternetFile` and frees any of its resources.  
  
## Syntax  
  
```  
  
virtual void Close( );  
  
```  
  
## Remarks  
 If the file was opened for writing, there is an implicit call to [Flush](../vs140/CInternetFile--Flush.md) to assure that all buffered data is written to the host. You should call **Close** when you are finished using a file.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException*`.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)