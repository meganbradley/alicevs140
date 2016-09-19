---
title: "DDV_MaxChars"
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
ms.assetid: 566a5ac5-c9d3-49e9-9dff-ce4197d008be
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDV_MaxChars
Call `DDV_MaxChars` to verify that the amount of characters in the control associated with *value* does not exceed *nChars*.  
  
## Syntax  
  
```  
  
      void AFXAPI DDV_MaxChars(  
   CDataExchange* pDX,  
   CString const& value,  
   int nChars   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 *value*  
 A reference to a member variable of the dialog box, form view, or control view object with which data is validated.  
  
 `nChars`  
 Maximum number of characters allowed.  
  
## Remarks  
 For more information about DDV, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Validation Routines](../vs140/Standard-Dialog-Data-Validation-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)