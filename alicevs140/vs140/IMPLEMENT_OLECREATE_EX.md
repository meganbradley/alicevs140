---
title: "IMPLEMENT_OLECREATE_EX"
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
ms.assetid: 81446997-47a9-47f2-9d15-d50b505f8510
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IMPLEMENT_OLECREATE_EX
Implements your control's class factory and the [GetClassID](../vs140/COleControl--GetClassID.md) member function of your control class.  
  
## Syntax  
  
```  
  
IMPLEMENT_OLECREATE_EX(  
class_name  
,   
external_name  
,   
l  
,   
w1  
,   
w2  
,   
b1  
,   
b2  
,   
b3  
,   
b4  
,   
b5  
,   
b6  
,   
b7  
,   
b8 )  
```  
  
#### Parameters  
 *class_name*  
 The name of the control property page class.  
  
 *external_name*  
 The object name exposed to applications.  
  
 *l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8*  
 Components of the class's **CLSID**. For more information on these parameters, see the Remarks for [IMPLEMENT_OLECREATE](../vs140/IMPLEMENT_OLECREATE.md).  
  
## Remarks  
 This macro must appear in the implementation file for any control class that uses the `DECLARE_OLECREATE_EX` macro or the `BEGIN_OLEFACTORY` and `END_OLEFACTORY` macros. The external name is the identifier of the OLE control that is exposed to other applications. Containers use this name to request an object of this control class.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DECLARE_OLECREATE_EX](../vs140/DECLARE_OLECREATE_EX.md)   
 [BEGIN_OLEFACTORY](../vs140/BEGIN_OLEFACTORY.md)   
 [END_OLEFACTORY](../vs140/END_OLEFACTORY.md)   
 [IMPLEMENT_OLECREATE](../vs140/IMPLEMENT_OLECREATE.md)