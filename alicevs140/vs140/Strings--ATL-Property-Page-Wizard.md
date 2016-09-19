---
title: "Strings, ATL Property Page Wizard"
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
ms.assetid: 00547db6-911f-49eb-92e1-2ba67079d4df
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Strings, ATL Property Page Wizard
Provides the text associated with the property page.  
  
 **Title**  
 Sets the text that appears on the tab of the property page.  
  
 **Doc string**  
 Sets a text string describing the page. This string can be displayed in the property sheet dialog box. The property frame could use the description in a status line or tool tip. The standard property frame currently does not use this string.  
  
 **Help file**  
 Sets the name of the help file that describes how to use the property page. This name should not include a path. When the user presses **Help**, the frame opens the help file in the directory named in the value of the HelpDir key in the property page registry entries under its CLSID.  
  
## See Also  
 [ATL Property Page Wizard](../vs140/ATL-Property-Page-Wizard.md)   
 [Options, ATL Property Page Wizard](../vs140/Options--ATL-Property-Page-Wizard.md)