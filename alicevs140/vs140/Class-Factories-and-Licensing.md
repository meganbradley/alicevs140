---
title: "Class Factories and Licensing"
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
ms.assetid: 53c4856a-4062-46db-9f69-dd4339f746b3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Class Factories and Licensing
To create an instance of your OLE control, a container application calls a member function of the control's class factory. Because your control is an actual OLE object, the class factory is responsible for creating instances of your control. Every OLE control class must have a class factory.  
  
 Another important feature of OLE controls is their ability to enforce a license. ControlWizard allows you to incorporate licensing during the creation of your control project. For more information on control licensing, see the article [ActiveX Controls: Licensing An ActiveX Control](../vs140/MFC-ActiveX-Controls--Licensing-an-ActiveX-Control.md).  
  
 The following table lists several macros and functions used to declare and implement your control's class factory and to license of your control.  
  
### Class Factories and Licensing  
  
|||  
|-|-|  
|[DECLARE_OLECREATE_EX](../vs140/DECLARE_OLECREATE_EX.md)|Declares the class factory for an OLE control or property page.|  
|[IMPLEMENT_OLECREATE_EX](../vs140/IMPLEMENT_OLECREATE_EX.md)|Implements the control's `GetClassID` function and declares an instance of the class factory.|  
|[BEGIN_OLEFACTORY](../vs140/BEGIN_OLEFACTORY.md)|Begins the declaration of any licensing functions.|  
|[END_OLEFACTORY](../vs140/END_OLEFACTORY.md)|Ends the declaration of any licensing functions.|  
|[AfxVerifyLicFile](../vs140/AfxVerifyLicFile.md)|Verifies whether a control is licensed for use on a particular computer.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)