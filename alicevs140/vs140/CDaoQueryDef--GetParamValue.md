---
title: "CDaoQueryDef::GetParamValue"
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
ms.assetid: 3e60e1c0-c1bb-4333-b3d0-5be092734ac1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetParamValue
Call this member function to retrieve the current value of the specified parameter stored in the querydef's Parameters collection.  
  
## Syntax  
  
```  
  
      virtual COleVariant GetParamValue(   
   LPCTSTR lpszName    
);  
virtual COleVariant GetParamValue(   
   int nIndex    
);  
```  
  
#### Parameters  
 `lpszName`  
 The name of the parameter whose value you want, for lookup by name.  
  
 `nIndex`  
 The zero-based index of the parameter in the querydef's Parameters collection, for lookup by index. You can obtain this value with calls to [GetParameterCount](../vs140/CDaoQueryDef--GetParameterCount.md) and [GetParameterInfo](../vs140/CDaoQueryDef--GetParameterInfo.md).  
  
## Return Value  
 An object of class [COleVariant](../vs140/COleVariant-Class.md) that contains the parameter's value.  
  
## Remarks  
 You can access the parameter either by name or by its ordinal position in the collection.  
  
 For related information, see the topic "PARAMETERS Declaration (SQL)" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::SetParamValue](../vs140/CDaoQueryDef--SetParamValue.md)