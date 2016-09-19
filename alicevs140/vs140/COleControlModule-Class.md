---
title: "COleControlModule Class"
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
ms.topic: reference
ms.assetid: 0721724d-d4af-4eda-ad34-5a2b27810dd4
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlModule Class
The base class from which you derive an OLE control module object.  
  
## Syntax  
  
```  
class COleControlModule : public CWinApp  
```  
  
## Remarks  
 This class provides member functions for initializing your control module. Each OLE control module that uses the Microsoft Foundation classes can only contain one object derived from `COleControlModule`. This object is constructed when other C++ global objects are constructed. Declare your derived `COleControlModule` object at the global level.  
  
 For more information on using the `COleControlModule` class, see the [CWinApp](../vs140/CWinApp-Class.md) class and the article [ActiveX Controls](../vs140/MFC-ActiveX-Controls.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWinThread](../vs140/CWinThread-Class.md)  
  
 [CWinApp](../vs140/CWinApp-Class.md)  
  
 `COleControlModule`  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [MFC Sample TESTHELP](../vs140/Visual-C---Samples.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)