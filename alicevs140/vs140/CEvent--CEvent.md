---
title: "CEvent::CEvent"
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
ms.assetid: 887031a7-39e7-4ad6-aa6d-c6226930b775
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEvent::CEvent
Constructs a named or unnamed `CEvent` object.  
  
## Syntax  
  
```  
  
      CEvent(  
   BOOL bInitiallyOwn = FALSE,  
   BOOL bManualReset = FALSE,  
   LPCTSTR lpszName = NULL,  
   LPSECURITY_ATTRIBUTES lpsaAttribute = NULL   
);  
```  
  
#### Parameters  
 `bInitiallyOwn`  
 If **TRUE**, the thread for the **CMultilock** or `CSingleLock` object is enabled. Otherwise, all threads wanting to access the resource must wait.  
  
 *bManualReset*  
 If **TRUE**, specifies that the event object is a manual event, otherwise the event object is an automatic event.  
  
 `lpszName`  
 Name of the `CEvent` object. Must be supplied if the object will be used across process boundaries. If the name matches an existing event, the constructor builds a new `CEvent` object which references the event of that name. If the name matches an existing synchronization object that is not an event, the construction will fail. If **NULL**, the name will be null.  
  
 `lpsaAttribute`  
 Security attributes for the event object. For a full description of this structure, see [SECURITY_ATTRIBUTES](http://msdn.microsoft.com/library/windows/desktop/aa379560) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 To access or release a `CEvent` object, create a [CMultiLock](../vs140/CMultiLock-Class.md) or [CSingleLock](../vs140/CSingleLock-Class.md) object and call its [Lock](../vs140/CSingleLock--Lock.md) and [Unlock](../vs140/CSingleLock--Unlock.md) member functions.  
  
 To change the state of a `CEvent` object to signaled (threads do not have to wait), call [SetEvent](../vs140/CEvent--SetEvent.md) or [PulseEvent](../vs140/CEvent--PulseEvent.md). To set the state of a `CEvent` object to nonsignaled (threads must wait), call [ResetEvent](../vs140/CEvent--ResetEvent.md).  
  
> [!IMPORTANT]
>  After creating the `CEvent` object, use [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) to ensure that the mutex didn't already exist. If the mutex did exist unexpectedly, it may indicate a rogue process is squatting and may be intending to use the mutex maliciously. In this case, the recommended security-conscious procedure is to close the handle and continue as if there was a failure in creating the object.  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CEvent Class](../vs140/CEvent-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)