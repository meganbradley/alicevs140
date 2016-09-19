---
title: "COleControl::SetInitialDataFormats"
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
ms.assetid: 58488a91-8966-4c10-928c-190c370426ca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetInitialDataFormats
Called by the framework to initialize the list of data formats supported by the control.  
  
## Syntax  
  
```  
  
virtual void SetInitialDataFormats( );  
```  
  
## Remarks  
 The default implementation specifies two formats: `CF_METAFILEPICT` and the persistent property set.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)