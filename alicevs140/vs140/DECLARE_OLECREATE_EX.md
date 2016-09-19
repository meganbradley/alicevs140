---
title: "DECLARE_OLECREATE_EX"
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
ms.assetid: 8b77d83a-845b-45bf-b403-015dafa14f1e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_OLECREATE_EX
Declares a class factory and the `GetClassID` member function of your control class.  
  
## Syntax  
  
```  
  
DECLARE_OLECREATE_EX(  
class_name )  
```  
  
#### Parameters  
 *class_name*  
 The name of the control class.  
  
## Remarks  
 Use this macro in the control class header file for a control that does not support licensing.  
  
 Note that this macro serves the same purpose as the following code sample:  
  
 [!CODE [NVC_MFCAxCtl#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#14)]  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_OLEFACTORY](../vs140/BEGIN_OLEFACTORY.md)   
 [END_OLEFACTORY](../vs140/END_OLEFACTORY.md)