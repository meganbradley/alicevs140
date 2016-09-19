---
title: "COleStreamFile::COleStreamFile"
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
ms.assetid: c179a5f4-fa6c-4968-80b4-1f417d929c6e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleStreamFile::COleStreamFile
Creates a `COleStreamFile` object.  
  
## Syntax  
  
```  
  
      COleStreamFile(  
   LPSTREAM lpStream = NULL   
);  
```  
  
#### Parameters  
 `lpStream`  
 Pointer to the OLE stream to be associated with the object.  
  
## Remarks  
 If `lpStream` is **NULL**, the object is not associated with an OLE stream, otherwise, the object is associated with the supplied OLE stream.  
  
 For more information, see [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleStreamFile Class](../vs140/COleStreamFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleStreamFile::Attach](../vs140/COleStreamFile--Attach.md)   
 [CFile Class](../vs140/CFile-Class.md)