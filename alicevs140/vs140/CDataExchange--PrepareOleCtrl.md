---
title: "CDataExchange::PrepareOleCtrl"
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
ms.assetid: d6cc720d-b5ae-4d79-b8f8-6d7bca9b4ffd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataExchange::PrepareOleCtrl
The framework calls this member function to prepare the specified OLE control for dialog data exchange (DDX) and validation (DDV).  
  
## Syntax  
  
```  
  
      COleControlSite* PrepareOleCtrl(  
   int nIDC  
);  
```  
  
#### Parameters  
 `nIDC`  
 The ID of the OLE control to be prepared for DDX or DDV.  
  
## Return Value  
 A pointer to the OLE control site.  
  
## Remarks  
 Use [PrepareEditCtrl](../vs140/CDataExchange--PrepareEditCtrl.md) instead for edit controls or [PrepareCtrl](../vs140/CDataExchange--PrepareCtrl.md) for all other non-OLE controls.  
  
 Implementors of custom DDX or DDV routines should call `PrepareOleCtrl` for all OLE controls for which they are exchanging data via DDX or validating data via DDV.  
  
 For more information on writing your own DDX and DDV routines, see [Technical Note 26](../vs140/TN026--DDX-and-DDV-Routines.md). For an overview of DDX and DDV, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md) and [Dialog Box Topics](../vs140/Dialog-Boxes.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDataExchange Class](../vs140/CDataExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)