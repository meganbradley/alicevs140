---
title: "DDX_Control"
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
ms.assetid: 8d51aeb2-d8ae-4f09-9945-6f365fa5e70d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_Control
The `DDX_Control` function subclasses the control, specified by `nIDC`, of the dialog box, form view, or control view object.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_Control(  
   CDataExchange* pDX,  
   int nIDC,  
   CWnd& rControl   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object.  
  
 `nIDC`  
 The resource ID of the control to be subclassed.  
  
 *rControl*  
 A reference to a member variable of the dialog box, form view, or control view object related to the specified control.  
  
## Remarks  
 The `pDX` object is supplied by the framework when the `DoDataExchange` function is called. Therefore, `DDX_Control` should only be called within your override of `DoDataExchange`.  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Exchange Routines](../vs140/Standard-Dialog-Data-Exchange-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)