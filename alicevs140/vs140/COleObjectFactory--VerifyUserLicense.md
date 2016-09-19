---
title: "COleObjectFactory::VerifyUserLicense"
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
ms.assetid: 6477d1f0-4dfb-42ef-bf38-0abb1385aec1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::VerifyUserLicense
Verifies the design-time license for the OLE control.  
  
## Syntax  
  
```  
  
virtual BOOL VerifyUserLicense( );  
```  
  
## Return Value  
 Nonzero if the design-time license is valid; otherwise 0.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::VerifyLicenseKey](../vs140/COleObjectFactory--VerifyLicenseKey.md)   
 [COleObjectFactory::GetLicenseKey](../vs140/COleObjectFactory--GetLicenseKey.md)