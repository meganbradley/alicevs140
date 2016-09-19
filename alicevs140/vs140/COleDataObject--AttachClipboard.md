---
title: "COleDataObject::AttachClipboard"
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
ms.assetid: 0eef77f9-94bd-4523-96f2-254caffdc53a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataObject::AttachClipboard
Call this function to attach the data object that is currently on the Clipboard to the `COleDataObject` object.  
  
## Syntax  
  
```  
  
BOOL AttachClipboard( );  
```  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
  
> [!NOTE]
>  Calling this function locks the Clipboard until this data object is released. The data object is released in the destructor for the `COleDataObject`. For more information, see [OpenClipboard](http://msdn.microsoft.com/library/windows/desktop/ms649048) and [CloseClipboard](http://msdn.microsoft.com/library/windows/desktop/ms649035) in the Win32 documention.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject::Attach](../vs140/COleDataObject--Attach.md)   
 [COleDataObject::Detach](../vs140/COleDataObject--Detach.md)   
 [COleDataObject::Release](../vs140/COleDataObject--Release.md)