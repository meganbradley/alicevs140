---
title: "Stock Properties"
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
ms.assetid: a89fc454-0b8e-447a-9033-4c8af46a24d9
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Stock Properties
If you are adding a property to an MFC dispinterface using the [Add Property Wizard](../vs140/IDL-Attributes--Add-Property-Wizard.md), you can choose a stock property from the **Property name** list in the [Names](../vs140/Names--Add-Property-Wizard.md) page of the wizard. These properties are as follows:  
  
|Property name|Description|  
|-------------------|-----------------|  
|**Appearance**|Returns or sets a value that determines the appearance of the control. The control's **Appearance** property can include or omit three-dimensional display effects. This is an ambient read/write property.|  
|`BackColor`|Returns or sets the control's ambient `BackColor` property to either a palette (RGB) color or a predefined system color. By default, its value corresponds to the foreground color of the control's container. This is an ambient read/write property.|  
|`BorderStyle`|Returns or sets the border style for a control. This is a read/write property.|  
|**Caption**|Returns or sets the control's **Caption** property. The caption is the title of the window. **Caption** has no **Member variable** implementation type.|  
|**Enabled**|Returns or sets the control's **Enabled** property. An enabled control can respond to user-generated events.|  
|**Font**|Returns or sets the control's ambient font. Null if the control has no font.|  
|`ForeColor`|Returns or sets the control's ambient `ForeColor` property.|  
|**hWnd**|Returns or sets the control's **hWnd** property. **hWnd** has no **Member variable** implementation type.|  
|**ReadyState**|Returns or sets the control's **ReadyState** property. A control can be uninitialized, initialized, loading, interactive, or complete. See [READYSTATE](https://msdn.microsoft.com/en-us/library/aa768362.aspx) in the *Internet SDK* for more information.|  
|**Text**|Returns or sets the text contained in a control. **Text** has no **Member variable** implementation type.|  
  
## See Also  
 [Adding a Property](../vs140/Adding-a-Property--Visual-C---.md)   
 [IDL Attributes, Add Property Wizard](../vs140/IDL-Attributes--Add-Property-Wizard.md)