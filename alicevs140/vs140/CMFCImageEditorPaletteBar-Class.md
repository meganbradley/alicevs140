---
title: "CMFCImageEditorPaletteBar Class"
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
ms.assetid: 3fb7ba8e-f254-4d56-b913-9941b4ed8138
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCImageEditorPaletteBar Class
Provides palette bar functionality to an image editor dialog box.  
  
## Syntax  
  
```  
class CMFCImageEditorPaletteBar : public CMFCToolBar  
```  
  
## Members  
  
### Public Methods  
  
|||  
|-|-|  
|Name|Description|  
|[CMFCImageEditorPaletteBar::GetRowHeight](#cmfcimageeditorpalettebar__getrowheight)|Returns the height of toolbar buttons. (Overrides [CMFCToolBar::GetRowHeight](../Topic/CMFCToolBar%20Class.md#cmfctoolbar__getrowheight).)|  
|[CMFCImageEditorPaletteBar::IsButtonExtraSizeAvailable](#cmfcimageeditorpalettebar__isbuttonextrasizeavailable)|Determines whether the toolbar can display buttons that have extended borders. (Overrides [CMFCToolBar::IsButtonExtraSizeAvailable](../Topic/CMFCToolBar%20Class.md#cmfctoolbar__isbuttonextrasizeavailable).)|  
  
### Remarks  
 This class is not intended to be used directly from your code.  
  
 The framework uses this class to display a palette bar in an image editor dialog box. For more information about the image editor dialog box, see [CMFCImageEditorDialog Class](../vs140/CMFCImageEditorDialog-Class.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CBasePane](../vs140/CBasePane-Class.md)  
  
 [CPane](../vs140/CPane-Class.md)  
  
 [CMFCBaseToolBa](../vs140/CMFCBaseToolBar-Class.md)  
  
 [CMFCToolBar](../Topic/CMFCToolBar%20Class.md)  
  
 [CMFCImageEditorPaletteBar](../vs140/CMFCImageEditorPaletteBar-Class.md)  
  
## Requirements  
 **Header:** afximageeditordialog.h  
  
##  <a name="cmfcimageeditorpalettebar__getrowheight"></a>  CMFCImageEditorPaletteBar::GetRowHeight  
 Returns the height of toolbar buttons.  
  
```  
virtual int GetRowHeight() const;  
```  
  
### Return Value  
 The height of each button on the toolbar.  
  
##  <a name="cmfcimageeditorpalettebar__isbuttonextrasizeavailable"></a>  CMFCImageEditorPaletteBar::IsButtonExtraSizeAvailable  
 Determines whether the toolbar can display buttons that have extended borders.  
  
```  
virtual BOOL IsButtonExtraSizeAvailable() const;  
```  
  
### Return Value  
 This method returns `FALSE`.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCImageEditorDialog Class](../vs140/CMFCImageEditorDialog-Class.md)