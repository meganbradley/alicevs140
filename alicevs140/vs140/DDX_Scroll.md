---
title: "DDX_Scroll"
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
ms.assetid: 8514c532-2d6f-47ca-92cb-9121f0bb80c6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_Scroll
The `DDX_Scroll` function manages the transfer of `int` data between a scroll-bar control in a dialog box, form view, or control view object and an `int` data member of the dialog box, form view, or control view object.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_Scroll(  
   CDataExchange* pDX,  
   int nIDC,  
   int& value   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The resource ID of the scroll-bar control associated with the control property.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
## Remarks  
 When `DDX_Scroll` is called, *value* is set to the current position of the control's thumb. For more information on the values associated with the current position of the control's thumb, see [GetScrollPos](http://msdn.microsoft.com/library/windows/desktop/bb787585) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Exchange Routines](../vs140/Standard-Dialog-Data-Exchange-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_OCText](../vs140/DDX_OCText.md)