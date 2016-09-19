---
title: "CMFCRibbonApplicationButton Class"
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
ms.assetid: beb81757-fabd-4641-9130-876ba8505b78
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonApplicationButton Class
Implements a special button located in the top-left corner of the application window. When clicked, the button opens a menu that usually contains common **File** commands like **Open**, **Save**, and **Exit**.  
  
## Syntax  
  
```  
class CMFCRibbonApplicationButton : public CMFCRibbonButton  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCRibbonApplicationButton::CMFCRibbonApplicationButton](#cmfcribbonapplicationbutton__cmfcribbonapplicationbutton)|Constructs and initializes a `CMFCRibbonApplicationButton` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|`CMFCRibbonApplicationButton::CreateObject`|Used by the framework to create a dynamic instance of this class type.|  
|`CMFCRibbonApplicationButton::GetThisClass`|Used by the framework to obtain a pointer to the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) object that is associated with this class type.|  
|[CMFCRibbonApplicationButton::SetImage](#cmfcribbonapplicationbutton__setimage)|Assigns an image to the ribbon application button.|  
  
## Example  
 The following example demonstrates how to use various methods in the `CMFCRibbonApplicationButton` class. The example shows how to assign an image to the application button, and how to set its tooltip. This code snippet is part of the [Draw Client sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_DrawClient#4](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_DrawClient#4)]  
[!CODE [NVC_MFC_DrawClient#5](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_DrawClient#5)]  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CMFCRibbonBaseElement](../vs140/CMFCRibbonBaseElement-Class.md)  
  
 [CMFCRibbonButton](../vs140/CMFCRibbonButton-Class.md)  
  
 [CMFCRibbonApplicationButton](../vs140/CMFCRibbonApplicationButton-Class.md)  
  
## Requirements  
 **Header:** afxRibbonBar.h  
  
##  <a name="cmfcribbonapplicationbutton__cmfcribbonapplicationbutton"></a>  CMFCRibbonApplicationButton::CMFCRibbonApplicationButton  
 Constructs and initializes a [CMFCRibbonApplicationButton](../vs140/CMFCRibbonApplicationButton-Class.md) object.  
  
```  
CMFCRibbonApplicationButton();  
CMFCRibbonApplicationButton(  
   UINT uiBmpResID   
);  
CMFCRibbonApplicationButton(  
   HBITMAP hBmp   
);  
```  
  
### Parameters  
 `uiBmpResID`  
 The resource ID of the image to display on the application button.  
  
 `hBmp`  
 A handle to a bitmap to display on the application button.  
  
### Remarks  
 The ribbon application button is a special button that is located in the upper-left corner of the application window. When a user clicks this button, the application opens a menu that usually contains common **File** commands, such as **Open**, **Save**, and **Exit**.  
  
##  <a name="cmfcribbonapplicationbutton__setimage"></a>  CMFCRibbonApplicationButton::SetImage  
 Assigns an image to the application button.  
  
```  
void SetImage(  
   UINT uiBmpResID   
);  
void SetImage(  
   HBITMAP hBmp   
);  
```  
  
### Parameters  
 [in] `uiBmpResID`  
 The resource ID of the image to display on the application button.  
  
 [in] `hBmp`  
 A handle to a bitmap to display on the application button.  
  
### Remarks  
 Use this method to assign a new image to the ribbon application button after you create the button. The application button is located in the upper-left corner of the application window.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)