---
title: "AfxOleUnregisterTypeLib"
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
ms.assetid: 21daba2a-69ce-4124-be3c-d4eb9aca97f6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleUnregisterTypeLib
Call this function to remove the type library entry from the Windows registration database.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxOleUnregisterTypeLib(  
   REFGUID tlID   
);  
```  
  
#### Parameters  
 `tlID`  
 The unique ID of the type library.  
  
## Return Value  
 Nonzero if the type library was successfully unregistered; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCAxCtl#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#13)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxOleUnregisterClass](../vs140/AfxOleUnregisterClass.md)   
 [AfxOleRegisterTypeLib](../vs140/AfxOleRegisterTypeLib.md)