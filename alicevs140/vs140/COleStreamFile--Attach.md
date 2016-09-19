---
title: "COleStreamFile::Attach"
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
ms.assetid: 42e11c35-aca6-40b5-92f3-659497830575
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleStreamFile::Attach
Associates the supplied OLE stream with the `COleStreamFile` object.  
  
## Syntax  
  
```  
  
      void Attach(  
   LPSTREAM lpStream   
);  
```  
  
#### Parameters  
 `lpStream`  
 Points to the OLE stream (`IStream`) to be associated with the object. Cannot be **NULL**.  
  
## Remarks  
 The object must not already be associated with an OLE stream.  
  
 For more information, see [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleStreamFile Class](../vs140/COleStreamFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleStreamFile::Detach](../vs140/COleStreamFile--Detach.md)