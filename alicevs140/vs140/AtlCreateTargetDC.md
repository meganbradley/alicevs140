---
title: "AtlCreateTargetDC"
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
ms.assetid: 71cdcbd2-c7a1-479c-9b12-f511bb79353d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlCreateTargetDC
Creates a device context for the device specified in the [DVTARGETDEVICE](http://msdn.microsoft.com/library/windows/desktop/ms686613) structure.  
  
## Syntax  
  
```  
  
      HDC AtlCreateTargetDC(  
   HDC hdc,  
   DVTARGETDEVICE* ptd   
);  
```  
  
#### Parameters  
 *hdc*  
 [in] The existing handle of a device context, or **NULL**.  
  
 `ptd`  
 [in] A pointer to the **DVTARGETDEVICE** structure that contains information about the target device.  
  
## Return Value  
 Returns the handle to a device context for the device specified in the **DVTARGETDEVICE**. If no device is specified, returns the handle to the default display device.  
  
## Remarks  
 If the structure is **NULL** and *hdc* is **NULL**, creates a device context for the default display device.  
  
 If *hdc* is not **NULL** and `ptd` is **NULL**, the function returns the existing *hdc*.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Device Context Global Functions](../vs140/Device-Context-Global-Functions.md)