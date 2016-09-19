---
title: "CAsyncMonikerFile::GetFormatEtc"
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
ms.assetid: 5fb0220f-467e-4c4c-844f-9793dba78469
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncMonikerFile::GetFormatEtc
Call this function to retrieve the format of the data in the stream.  
  
## Syntax  
  
```  
  
FORMATETC* GetFormatEtc( ) const;  
```  
  
## Return Value  
 A pointer to the Windows structure [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) for the currently opened stream. Returns **NULL** if the moniker has not been bound, if it is not asynchronous, or if the asynchronous operation has not begun.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CAsyncMonikerFile Class](../vs140/CAsyncMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)