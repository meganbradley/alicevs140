---
title: "CMFCButton::SetMouseCursor"
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
ms.assetid: d9b09dca-743d-4cf0-8147-a43364ccef35
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::SetMouseCursor
Sets the cursor image.  
  
## Syntax  
  
```  
void SetMouseCursor(  
   HCURSOR hcursor   
);  
```  
  
#### Parameters  
 [in] `hcursor`  
 The handle of a cursor.  
  
## Remarks  
 Use this method to associate a cursor image, such as the hand cursor, with the button. The cursor is loaded from the application resources.  
  
## Example  
 The following example demonstrates how to use the `SetMouseCursor` method in the `CMFCButton` class. The example is part of the code in the [New Controls sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_NewControls#28](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#28)]  
[!CODE [NVC_MFC_NewControls#30](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#30)]  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCButton::SetMouseCursorHand](../vs140/CMFCButton--SetMouseCursorHand.md)