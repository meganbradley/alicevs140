---
title: "Specifying Property Pages"
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
ms.assetid: ee8678cf-c708-49ab-b0ad-fc2db31f1ac3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specifying Property Pages
When you create an ActiveX control, you will often want to associate it with property pages that can be used to set the properties of your control. Control containers use the **ISpecifyPropertyPages** interface to find out which property pages can be used to set your control's properties. You will need to implement this interface on your control.  
  
 To implement **ISpecifyPropertyPages** using ATL, take the following steps:  
  
1.  Derive your class from [ISpecifyPropertyPagesImpl](../vs140/ISpecifyPropertyPagesImpl-Class.md).  
  
2.  Add an entry for **ISpecifyPropertyPages** to your class's COM map.  
  
3.  Add a [PROP_PAGE](../vs140/PROP_PAGE.md) entry to the property map for each page associated with your control.  
  
> [!NOTE]
>  When generating a standard control using the [ATL Control Wizard](../vs140/ATL-Control-Wizard.md), you will only have to add the `PROP_PAGE` entries to the property map. The wizard generates the necessary code for the other steps.  
  
 Well-behaved containers will display the specified property pages in the same order as the `PROP_PAGE` entries in the property map. Generally, you should put standard property page entries after the entries for your custom pages in the property map, so that users see the pages specific to your control first.  
  
## Example  
 The following class for a calendar control uses the **ISpecifyPropertyPages** interface to tell containers that its properties can be set using a custom date page and the stock color page.  
  
 [!CODE [NVC_ATL_Windowing#72](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#72)]  
  
## See Also  
 [Property Pages](../vs140/ATL-COM-Property-Pages.md)   
 [ATLPages Sample](../vs140/Visual-C---Samples.md)