---
title: "IPersistStorageImpl::Save"
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
ms.assetid: 40e24b54-35fe-4c87-ac84-84985f4c8eaf
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPersistStorageImpl::Save
Saves the object's properties to the specified storage.  
  
## Syntax  
  
```  
  
      STDMETHOD(Save)(  
   IStorage* pStorage,  
   BOOL fSameAsLoad   
);  
```  
  
## Remarks  
 The ATL implementation delegates to the [IPersistStreamInit](http://msdn.microsoft.com/library/windows/desktop/ms682273) interface. When **Save** is first called, it creates a stream named "Contents" on the specified storage. This stream is then used in later calls to **Save** and in calls to [Load](../vs140/IPersistStorageImpl--Load.md).  
  
 See [IPersistStorage:Save](http://msdn.microsoft.com/library/windows/desktop/ms680680) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IPersistStorageImpl Class](../vs140/IPersistStorageImpl-Class.md)   
 [IPersistStorageImpl::SaveCompleted](../vs140/IPersistStorageImpl--SaveCompleted.md)   
 [IStorage](http://msdn.microsoft.com/library/windows/desktop/aa380015)