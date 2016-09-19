---
title: "COleStreamFile::Detach"
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
ms.assetid: 0f13e536-ae87-4063-9ba2-a15353e4bab6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleStreamFile::Detach
Disassociates the stream from the object without closing the stream.  
  
## Syntax  
  
```  
  
LPSTREAM Detach( );  
```  
  
## Return Value  
 A pointer to the stream (`IStream`) that was associated with the object.  
  
## Remarks  
 The stream must be closed in some other fashion before the program terminates.  
  
 For more information, see [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleStreamFile Class](../vs140/COleStreamFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleStreamFile::Attach](../vs140/COleStreamFile--Attach.md)