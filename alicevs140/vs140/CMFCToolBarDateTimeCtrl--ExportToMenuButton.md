---
title: "CMFCToolBarDateTimeCtrl::ExportToMenuButton"
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
ms.assetid: dc1d605e-142c-484d-bb82-f8d6c09ad7bc
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::ExportToMenuButton
Copies text from the toolbar button to a menu.  
  
## Syntax  
  
```  
virtual BOOL ExportToMenuButton(  
   CMFCToolBarMenuButton& menuButton   
) const;  
```  
  
#### Parameters  
 [in] `menuButton`  
 A reference to the target menu button.  
  
## Return Value  
 This method returns `TRUE`.  
  
## Remarks  
 This method overrides the base class implementation ([CMFCToolBarButton::ExportToMenuButton](../vs140/CMFCToolBarButton--ExportToMenuButton.md)) by loading the string resource that is associated with the command ID of the control. For more information about string resources, see [CStringT::LoadString](../vs140/CStringT--LoadString.md).  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [CMFCToolBarButton::ExportToMenuButton](../vs140/CMFCToolBarButton--ExportToMenuButton.md)   
 [CStringT::LoadString](../vs140/CStringT--LoadString.md)