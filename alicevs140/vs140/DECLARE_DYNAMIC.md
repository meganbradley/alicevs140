---
title: "DECLARE_DYNAMIC"
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
ms.assetid: 77c33880-c42c-428c-8f9f-14fefd5f070d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_DYNAMIC
Adds the ability to access run-time information about an object's class when deriving a class from `CObject`.  
  
## Syntax  
  
```  
  
DECLARE_DYNAMIC(  
class_name )  
```  
  
#### Parameters  
 *class_name*  
 The actual name of the class.  
  
## Remarks  
 Add the `DECLARE_DYNAMIC` macro to the header (.h) module for the class, then include that module in all .cpp modules that need access to objects of this class.  
  
 If you use the **DECLARE**_**DYNAMIC** and `IMPLEMENT_DYNAMIC` macros as described, you can then use the `RUNTIME_CLASS` macro and the `CObject::IsKindOf` function to determine the class of your objects at run time.  
  
 If `DECLARE_DYNAMIC` is included in the class declaration, then `IMPLEMENT_DYNAMIC` must be included in the class implementation.  
  
 For more information on the `DECLARE_DYNAMIC` macro, see [CObject Class Topics](../vs140/Using-CObject.md).  
  
## Example  
 See the example for [IMPLEMENT_DYNAMIC](../vs140/IMPLEMENT_DYNAMIC.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [IMPLEMENT_DYNAMIC](../vs140/IMPLEMENT_DYNAMIC.md)   
 [DECLARE_DYNCREATE](../vs140/DECLARE_DYNCREATE.md)   
 [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md)   
 [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md)   
 [CObject::IsKindOf](../vs140/CObject--IsKindOf.md)