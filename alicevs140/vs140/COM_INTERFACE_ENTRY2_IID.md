---
title: "COM_INTERFACE_ENTRY2_IID"
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
ms.assetid: cd14fad1-d55b-4088-bb87-55b9d896e598
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY2_IID
Same as [COM_INTERFACE_ENTRY2](../vs140/COM_INTERFACE_ENTRY2.md), except you can specify a different IID.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY2_IID(   
iid  
,   
x  
,   
x2  
 )  
  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID you are specifying for the interface.  
  
 *x*  
 [in] The name of an interface that your class object derives from directly.  
  
 `x2`  
 [in] The name of a second interface that your class object derives from directly.  
  
## Remarks  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)