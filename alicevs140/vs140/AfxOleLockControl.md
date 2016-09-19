---
title: "AfxOleLockControl"
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
ms.assetid: 12b2cfb5-b98c-410c-a158-442842c5213d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleLockControl
Locks the class factory of the specified control so that dynamically created data associated with the control remains in memory.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxOleLockControl(  
   REFCLSID clsid   
);  
BOOL AFXAPI AfxOleLockControl(  
   LPCTSTR lpszProgID   
);  
```  
  
#### Parameters  
 `clsid`  
 The unique class ID of the control.  
  
 `lpszProgID`  
 The unique program ID of the control.  
  
## Return Value  
 Nonzero if the class factory of the control was successfully locked; otherwise 0.  
  
## Remarks  
 This can significantly speed up display of the controls. For example, once you create a control in a dialog box and lock the control with `AfxOleLockControl`, you do not need to create and kill it again every time the dialog is shown or destroyed. If the user opens and closes a dialog box repeatedly, locking your controls can significantly enhance performance. When you are ready to destroy the control, call `AfxOleUnlockControl`.  
  
## Example  
 [!CODE [NVC_MFCAutomation#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAutomation#6)]  
  
## Requirements  
 **Header:** <afxwin.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxOleUnlockControl](../vs140/AfxOleUnlockControl.md)