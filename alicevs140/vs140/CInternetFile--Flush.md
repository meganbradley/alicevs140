---
title: "CInternetFile::Flush"
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
ms.assetid: ac9eecd3-11f8-4fa7-81fc-234d2af818bd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetFile::Flush
Call this member function to flush the contents of the write buffer.  
  
## Syntax  
  
```  
  
virtual void Flush( );  
  
```  
  
## Remarks  
 Use `Flush` to assure that all data in memory has actually been written to the target machine and to assure your transaction with the host machine has been completed. `Flush` is only effective on `CInternetFile` objects opened for writing.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException*`.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)