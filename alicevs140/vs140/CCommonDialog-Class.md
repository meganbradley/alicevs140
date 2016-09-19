---
title: "CCommonDialog Class"
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
ms.assetid: 1f68d65f-a0fd-4778-be22-ebbe51a95f95
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommonDialog Class
The base class for classes that encapsulate functionality of the Windows common dialogs.  
  
## Syntax  
  
```  
class CCommonDialog : public CDialog  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CCommonDialog::CCommonDialog](#ccommondialog__ccommondialog)|Constructs a `CCommonDialog` object.|  
  
## Remarks  
 The following classes encapsulate the functionality of the Windows common dialogs:  
  
-   [CFileDialog](../vs140/CFileDialog-Class.md)  
  
-   [CFontDialog](../vs140/CFontDialog-Class.md)  
  
-   [CColorDialog](../vs140/CColorDialog-Class.md)  
  
-   [CPageSetupDialog](../vs140/CPageSetupDialog-Class.md)  
  
-   [CPrintDialog](../vs140/CPrintDialog-Class.md)  
  
-   [CPrintDialogEx](../vs140/CPrintDialogEx-Class.md)  
  
-   [CFindReplaceDialog](../vs140/CFindReplaceDialog-Class.md)  
  
-   [COleDialog](../vs140/COleDialog-Class.md)  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 `CCommonDialog`  
  
## Requirements  
 **Header:** afxdlgs.h  
  
##  <a name="ccommondialog__ccommondialog"></a>  CCommonDialog::CCommonDialog  
 Constructs a `CCommonDialog` object.  
  
```  
explicit CCommonDialog(    CWnd*  pParentWnd );  
  
```  
  
### Parameters  
 `pParentWnd`  
 Points to the parent or owner window object (of type [CWnd](../vs140/CWnd-Class.md)) to which the dialog object belongs. If it is **NULL**, the dialog object's parent window is set to the main application window.  
  
### Remarks  
 See [CDialog::CDialog](../vs140/CDialog-Class.md#cdialog__cdialog) for complete information.  
  
## See Also  
 [Base Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog](../vs140/CFileDialog-Class.md)   
 [CFontDialog](../vs140/CFontDialog-Class.md)   
 [CColorDialog](../vs140/CColorDialog-Class.md)   
 [CPageSetupDialog](../vs140/CPageSetupDialog-Class.md)   
 [CPrintDialog](../vs140/CPrintDialog-Class.md)   
 [CFindReplaceDialog](../vs140/CFindReplaceDialog-Class.md)   
 [COleDialog](../vs140/COleDialog-Class.md)