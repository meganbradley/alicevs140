---
title: "IPersistPropertyBagImpl::Save"
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
ms.assetid: 133739f8-2a0c-4594-a8f1-dacf5cf38e9b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPersistPropertyBagImpl::Save
Saves the object's properties into a client-supplied property bag.  
  
## Syntax  
  
```  
  
      STDMETHOD(Save)(  
   LPPROPERTYBAG pPropBag,  
   BOOL fClearDirty,  
   BOOL fSaveAllProperties   
);  
```  
  
## Remarks  
 ATL uses the object's property map to store this information. By default, this method saves all properties, regardless of the value of *fSaveAllProperties*.  
  
 See [IPersistPropertyBag::Save](https://msdn.microsoft.com/en-us/library/aa768207.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IPersistPropertyBagImpl Class](../vs140/IPersistPropertyBagImpl-Class.md)   
 [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md)   
 [IPersistPropertyBagImpl::Load](../vs140/IPersistPropertyBagImpl--Load.md)   
 [IPropertyBag](https://msdn.microsoft.com/en-us/library/aa768196.aspx)