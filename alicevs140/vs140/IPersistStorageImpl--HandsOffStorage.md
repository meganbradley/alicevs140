---
title: "IPersistStorageImpl::HandsOffStorage"
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
ms.assetid: d2f4501e-2c49-431a-a5be-76ed940a5760
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPersistStorageImpl::HandsOffStorage
Instructs the object to release all storage objects and enter HandsOff mode.  
  
## Syntax  
  
```  
  
STDMETHOD(HandsOffStorage)(void);  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 See [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/windows/desktop/ms679742) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IPersistStorageImpl Class](../vs140/IPersistStorageImpl-Class.md)   
 [IPersistStorageImpl::SaveCompleted](../vs140/IPersistStorageImpl--SaveCompleted.md)   
 [IPersistStorageImpl::Save](../vs140/IPersistStorageImpl--Save.md)