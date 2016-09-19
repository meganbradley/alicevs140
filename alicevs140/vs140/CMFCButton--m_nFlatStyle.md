---
title: "CMFCButton::m_nFlatStyle"
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
ms.assetid: 8a7326ec-4e18-4d83-af42-d2215dffdeb2
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::m_nFlatStyle
Specifies the style of the button, such as borderless, flat, semi-flat, or 3D.  
  
## Syntax  
  
```  
FlatStyle  m_nFlatStyle;  
```  
  
## Remarks  
 The following table lists the `CMFCButton::m_nFlatStyle` enumeration values that specify the appearance of a button.  
  
|Value|Description|  
|-----------|-----------------|  
|BUTTONSTYLE_3D|(Default) The button appears to have high, three-dimensional sides. When the button is clicked, the button appears to be pressed into a deep indentation.|  
|BUTTONSTYLE_FLAT|When the mouse does not pause over the button, the button appears to be two-dimensional and does not have raised sides. When the mouse pauses over the button, the button appears to have low, three-dimensional sides. When the button is clicked, the button appears to be pressed into a shallow indentation.|  
|BUTTONSTYLE_SEMIFLAT|The button appears to have low, three-dimensional sides. When the button is clicked, the button appears to be pressed into a deep indentation.|  
|BUTTONSTYLE_NOBORDERS|The button does not have raised sides and always appears two-dimensional. The button does not appear to be pressed into an indentation when it is clicked.|  
  
 The `CMFCButton` constructor initializes this member to `BUTTONSTYLE_3D`.  
  
## Example  
 The following example demonstrates how to set the values of the `m_nFlatStyle` member variable in the `CMFCButton` class. This example is part of the [New Controls sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_NewControls#28](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#28)]  
[!CODE [NVC_MFC_NewControls#29](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#29)]  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)