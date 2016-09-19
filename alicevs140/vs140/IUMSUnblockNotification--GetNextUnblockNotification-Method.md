---
title: "IUMSUnblockNotification::GetNextUnblockNotification Method"
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
ms.topic: article
ms.assetid: 536d6df0-a14c-47b9-b404-1952d4c44c1b
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IUMSUnblockNotification::GetNextUnblockNotification Method
Returns the next `IUMSUnblockNotification` interface in the chain returned from the method `IUMSCompletionList::GetUnblockNotifications`.  
  
## Syntax  
  
```  
virtual IUMSUnblockNotification* GetNextUnblockNotification() =0;  
```  
  
## Return Value  
 The next `IUMSUnblockNotification` interface in the chain returned from the method `IUMSCompletionList::GetUnblockNotifications`.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IUMSUnblockNotification Structure](../vs140/IUMSUnblockNotification-Structure.md)