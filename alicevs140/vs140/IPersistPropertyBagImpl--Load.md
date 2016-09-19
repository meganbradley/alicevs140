---
title: "IPersistPropertyBagImpl::Load"
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
ms.assetid: 4068f041-ff11-4b4d-977d-bdcf35cd4a51
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPersistPropertyBagImpl::Load
Loads the object's properties from a client-supplied property bag.  
  
## Syntax  
  
```  
  
      STDMETHOD(Load)(  
   LPPROPERTYBAG pPropBag,  
   LPERRORLOG pErrorLog   
);  
```  
  
## Remarks  
 ATL uses the object's property map to retrieve this information.  
  
 See [IPersistPropertyBag::Load](https://msdn.microsoft.com/en-us/library/aa768206.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IPersistPropertyBagImpl Class](../vs140/IPersistPropertyBagImpl-Class.md)   
 [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md)   
 [IPersistPropertyBagImpl::Save](../vs140/IPersistPropertyBagImpl--Save.md)   
 [IPropertyBag](https://msdn.microsoft.com/en-us/library/aa768196.aspx)   
 [IErrorLog](https://msdn.microsoft.com/en-us/library/aa768231.aspx)