---
title: "BEGIN_OLEFACTORY"
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
ms.assetid: d834f2ca-7a4a-49cd-8e4b-1bc4adb15af9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_OLEFACTORY
Begins the declaration of your class factory in the header file of your control class.  
  
## Syntax  
  
```  
  
BEGIN_OLEFACTORY(  
class_name )  
```  
  
#### Parameters  
 *class_name*  
 Specifies the name of the control class whose class factory this is.  
  
## Remarks  
 Declarations of class factory licensing functions should begin immediately after `BEGIN_OLEFACTORY`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [END_OLEFACTORY](../vs140/END_OLEFACTORY.md)   
 [DECLARE_OLECREATE_EX](../vs140/DECLARE_OLECREATE_EX.md)