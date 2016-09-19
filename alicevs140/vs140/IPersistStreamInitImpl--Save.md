---
title: "IPersistStreamInitImpl::Save"
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
ms.assetid: 1cefec59-c369-45bb-9360-16b5a13bea6a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPersistStreamInitImpl::Save
Saves the object's properties to the specified stream.  
  
## Syntax  
  
```  
  
      STDMETHOD(Save)(  
   LPSTREAM pStm,  
   BOOL fClearDirty   
);  
```  
  
## Remarks  
 ATL uses the object's property map to store this information.  
  
 See [IPersistStreamInit::Save](http://msdn.microsoft.com/library/windows/desktop/ms694439) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IPersistStreamInitImpl Class](../vs140/IPersistStreamInitImpl-Class.md)   
 [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md)   
 [IPersistStreamInitImpl::Load](../vs140/IPersistStreamInitImpl--Load.md)   
 [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034)