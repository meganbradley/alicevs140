---
title: "DDX_OCFloatRO"
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
ms.assetid: 29948545-fab9-4358-a0ae-df04d50b9711
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_OCFloatRO
The `DDX_OCFloatRO` function manages the transfer of **float** (or **double**) data between a read-only property of an OLE control in a dialog box, form view, or control view object and a **float** (or **double**) data member of the dialog box, form view, or control view object.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_OCFloatRO(  
   CDataExchange* pDX,  
   int nIDC,  
   DISPID dispid,  
   float& value   
);  
void AFXAPI DDX_OCFloatRO(  
   CDataExchange* pDX,  
   int nIDC,  
   DISPID dispid,  
   double& value   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
## Remarks  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_OCFloat](../vs140/DDX_OCFloat.md)