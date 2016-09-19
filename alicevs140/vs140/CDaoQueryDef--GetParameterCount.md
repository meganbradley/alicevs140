---
title: "CDaoQueryDef::GetParameterCount"
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
ms.assetid: b75f41e7-55dc-4b13-878e-f528c2df4423
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetParameterCount
Call this member function to retrieve the number of parameters in the saved query.  
  
## Syntax  
  
```  
  
short GetParameterCount( );  
  
```  
  
## Return Value  
 The number of parameters defined in the query.  
  
## Remarks  
 `GetParameterCount` is useful for looping through all parameters in the querydef. For that purpose, use `GetParameterCount` in conjunction with [GetParameterInfo](../vs140/CDaoQueryDef--GetParameterInfo.md).  
  
 For related information, see the topics "Parameter Object", "Parameters Collection", and "PARAMETERS Declaration (SQL)" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::GetParamValue](../vs140/CDaoQueryDef--GetParamValue.md)   
 [CDaoQueryDef::SetParamValue](../vs140/CDaoQueryDef--SetParamValue.md)