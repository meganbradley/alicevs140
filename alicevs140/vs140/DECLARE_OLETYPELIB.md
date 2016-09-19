---
title: "DECLARE_OLETYPELIB"
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
ms.assetid: b5574b62-d84d-4e3f-a8ff-be15edc1f632
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_OLETYPELIB
Declares the `GetTypeLib` member function of your control class.  
  
## Syntax  
  
```  
  
DECLARE_OLETYPELIB(  
class_name )  
```  
  
#### Parameters  
 *class_name*  
 The name of the control class related to the type library.  
  
## Remarks  
 Use this macro in the control class header file.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [IMPLEMENT_OLETYPELIB](../vs140/IMPLEMENT_OLETYPELIB.md)