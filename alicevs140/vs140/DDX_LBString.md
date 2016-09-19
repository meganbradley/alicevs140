---
title: "DDX_LBString"
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
ms.assetid: 93717c09-5e66-44bb-944b-e800c82ee874
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_LBString
The `DDX_LBString` function manages the transfer of `CString` data between a list box control in a dialog box, form view, or control view object and a `CString` data member of the dialog box, form view, or control view object.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_LBString(  
   CDataExchange* pDX,  
   int nIDC,  
   CString& value   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The resource ID of the list box control associated with the control property.  
  
 *value*  
 A reference to a member variable of the dialog box, form view, or control view object with which data is exchanged.  
  
## Remarks  
 When `DDX_LBString` is called to transfer data to a list box control, the first item in the control whose beginning matches *value* is selected. (To match the entire item rather than just a prefix, use [DDX_LBStringExact](../vs140/DDX_LBStringExact.md).) If there are no matches, no items are selected. The matching is case-insensitive.  
  
 When `DDX_LBString` is called to transfer data from a list box control, *value* is set to the current list box selection. If no item is selected, *value* is set to a string of zero length.  
  
> [!NOTE]
>  If the list box is a drop-down list box, the value exchanged is limited to 255 characters.  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Exchange Routines](../vs140/Standard-Dialog-Data-Exchange-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDP_LBString](../vs140/DDP_LBString.md)