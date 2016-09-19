---
title: "IPersistStreamInitImpl::GetSizeMax"
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
ms.assetid: a1b9dbb0-ad2d-4b9c-a095-9763d2b905f6
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPersistStreamInitImpl::GetSizeMax
Retrieves the size of the stream needed to save the object's data.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetSizeMax)(  
   ULARGE_INTEGER FAR* pcbSize   
);  
```  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 See [IPersistStreamInit::GetSizeMax](http://msdn.microsoft.com/library/windows/desktop/ms687287) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IPersistStreamInitImpl Class](../vs140/IPersistStreamInitImpl-Class.md)