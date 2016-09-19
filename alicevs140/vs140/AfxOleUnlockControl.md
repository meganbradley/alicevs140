---
title: "AfxOleUnlockControl"
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
ms.assetid: 721503cb-c47a-40c3-b620-f870b2980f26
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleUnlockControl
Unlocks the class factory of the specified control.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxOleUnlockControl(  
   REFCLSID clsid   
);  
BOOL AFXAPI AfxOleUnlockControl(  
   LPCTSTR lpszProgID   
);  
```  
  
#### Parameters  
 `clsid`  
 The unique class ID of the control.  
  
 `lpszProgID`  
 The unique program ID of the control.  
  
## Return Value  
 Nonzero if the class factory of the control was successfully unlocked; otherwise 0.  
  
## Remarks  
 A control is locked with `AfxOleLockControl`, so that dynamically created data associated with the control remains in memory. This can significantly speed up display of the control because the control need not be created and destroyed every time it is displayed. When you are ready to destroy the control, call `AfxOleUnlockControl`.  
  
## Example  
 [!CODE [NVC_MFCAutomation#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAutomation#9)]  
  
## Requirements  
 **Header:** <afxwin.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxOleLockControl](../vs140/AfxOleLockControl.md)