---
title: "CMonikerFile::Detach"
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
ms.assetid: 77858a52-23c9-4fd6-af70-64a79fc23054
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonikerFile::Detach
Call this function to close the stream.  
  
## Syntax  
  
```  
  
      BOOL Detach(  
   CFileException* pError = NULL   
);  
```  
  
#### Parameters  
 `pError`  
 A pointer to a file exception. In the event of an error, it will be set to the cause.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CMonikerFile Class](../vs140/CMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonikerFile::Close](../vs140/CMonikerFile--Close.md)   
 [CMonikerFile::Open](../vs140/CMonikerFile--Open.md)