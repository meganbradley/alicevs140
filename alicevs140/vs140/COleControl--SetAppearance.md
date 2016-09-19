---
title: "COleControl::SetAppearance"
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
ms.assetid: 68c9c2d0-0972-44e0-95fd-53efc2a7b905
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetAppearance
Sets the stock Appearance property value of your control.  
  
## Syntax  
  
```  
  
      void SetAppearance (  
   short sAppearance   
);  
```  
  
#### Parameters  
 *sAppearance*  
 A **short** (`VT_I2`) value to be used for the appearance of your control. A value of zero sets the control's appearance to flat and a value of 1 sets the control's appearance to 3D.  
  
## Remarks  
 For more about stock properties, see [ActiveX Controls: Properties](../vs140/MFC-ActiveX-Controls--Properties.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetAppearance](../vs140/COleControl--GetAppearance.md)   
 [COleControl::OnAppearanceChanged](../vs140/COleControl--OnAppearanceChanged.md)