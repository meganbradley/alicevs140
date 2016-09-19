---
title: "COleObjectFactory::VerifyLicenseKey"
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
ms.assetid: a08b6d1b-d0cb-4ad6-b5f1-91b9a077af28
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::VerifyLicenseKey
Verifies that the container is licensed to use the OLE control.  
  
## Syntax  
  
```  
  
      virtual BOOL VerifyLicenseKey(  
   BSTR bstrKey   
);  
```  
  
#### Parameters  
 `bstrKey`  
 A `BSTR` storing the container's version of the license string.  
  
## Return Value  
 Nonzero if the run-time license is valid; otherwise 0.  
  
## Remarks  
 The default version calls [GetLicenseKey](../vs140/COleObjectFactory--GetLicenseKey.md) to get a copy of the control's license string and compares it with the string in `bstrKey`. If the two strings match, the function returns a nonzero value; otherwise it returns 0.  
  
 You can override this function to provide customized verification of the license.  
  
 The function [VerifyUserLicense](../vs140/COleObjectFactory--VerifyUserLicense.md) verifies the design-time license.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::VerifyUserLicense](../vs140/COleObjectFactory--VerifyUserLicense.md)   
 [COleObjectFactory::GetLicenseKey](../vs140/COleObjectFactory--GetLicenseKey.md)