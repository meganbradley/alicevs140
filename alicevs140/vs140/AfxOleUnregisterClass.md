---
title: "AfxOleUnregisterClass"
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
ms.topic: article
ms.assetid: c5235da2-9df8-449b-b307-2969890f2e68
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleUnregisterClass
Removes the control or property page class entry from the Windows registration database.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxOleUnregisterClass(  
   REFCLSID clsID,  
   LPCSTR pszProgID   
);  
```  
  
#### Parameters  
 *clsID*  
 The unique class ID of the control or property page.  
  
 `pszProgID`  
 The unique program ID of the control or property page.  
  
## Return Value  
 Nonzero if the control or property page class was successfully unregistered; otherwise 0.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxOleRegisterPropertyPageClass](../vs140/AfxOleRegisterPropertyPageClass.md)   
 [AfxOleRegisterControlClass](../vs140/AfxOleRegisterControlClass.md)   
 [AfxOleRegisterTypeLib](../vs140/AfxOleRegisterTypeLib.md)