---
title: "CAxDialogImpl::IsDialogMessage"
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
ms.assetid: 0c54e7ff-267a-4219-8bb6-f94234aba867
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxDialogImpl::IsDialogMessage
Call this method to determine whether a message is intended for this dialog box and, if it is, process the message.  
  
## Syntax  
  
```  
  
      BOOL IsDialogMessage(  
   LPMSG pMsg  
);  
```  
  
#### Parameters  
 `pMsg`  
 Pointer to a [MSG](http://msdn.microsoft.com/library/windows/desktop/ms644958) structure that contains the message to be checked.  
  
## Return Value  
 Returns TRUE if the message has been processed, FALSE otherwise.  
  
## Remarks  
 This method is intended to be called from within a message loop.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxDialogImpl Class](../vs140/CAxDialogImpl-Class.md)