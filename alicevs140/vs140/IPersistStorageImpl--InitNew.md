---
title: "IPersistStorageImpl::InitNew"
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
ms.assetid: a54ca482-92c5-44a7-b707-6a32ca170fb0
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPersistStorageImpl::InitNew
Initializes a new storage.  
  
## Syntax  
  
```  
  
      STDMETHOD(InitNew)(  
   IStorage*  
);  
```  
  
## Remarks  
 The ATL implementation delegates to the [IPersistStreamInit](http://msdn.microsoft.com/library/windows/desktop/ms682273) interface.  
  
 See [IPersistStorage:InitNew](http://msdn.microsoft.com/library/windows/desktop/ms687194) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IPersistStorageImpl Class](../vs140/IPersistStorageImpl-Class.md)   
 [IStorage](http://msdn.microsoft.com/library/windows/desktop/aa380015)