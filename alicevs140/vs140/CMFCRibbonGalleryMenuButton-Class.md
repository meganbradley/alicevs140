---
title: "CMFCRibbonGalleryMenuButton Class"
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
ms.assetid: 4d459d9b-8b1a-4371-92f6-dc4ce6cc42c8
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGalleryMenuButton Class
Implements a ribbon menu button that contains ribbon galleries.  
  
## Syntax  
  
```  
class CMFCRibbonGalleryMenuButton : public CMFCToolBarMenuButton  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCRibbonGalleryMenuButton::CMFCRibbonGalleryMenuButton](#cmfcribbongallerymenubutton__cmfcribbongallerymenubutton)|Constructs and initializes a `CMFCRibbonGalleryMenuButton` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCRibbonGalleryMenuButton::CopyFrom](#cmfcribbongallerymenubutton__copyfrom)|(Overrides [CMFCToolBarMenuButton::CopyFrom](../vs140/CMFCToolBarMenuButton-Class.md#cmfctoolbarmenubutton__copyfrom).)|  
|[CMFCRibbonGalleryMenuButton::CreatePopupMenu](#cmfcribbongallerymenubutton__createpopupmenu)|(Overrides [CMFCToolBarMenuButton::CreatePopupMenu](../vs140/CMFCToolBarMenuButton-Class.md#cmfctoolbarmenubutton__createpopupmenu).)|  
|[CMFCRibbonGalleryMenuButton::GetPalette](#cmfcribbongallerymenubutton__getpalette)||  
|[CMFCRibbonGalleryMenuButton::HasButton](#cmfcribbongallerymenubutton__hasbutton)|(Overrides `CMFCToolBarMenuButton::HasButton`.)|  
|[CMFCRibbonGalleryMenuButton::IsEmptyMenuAllowed](#cmfcribbongallerymenubutton__isemptymenuallowed)|(Overrides [CMFCToolBarMenuButton::IsEmptyMenuAllowed](../vs140/CMFCToolBarMenuButton-Class.md#cmfctoolbarmenubutton__isemptymenuallowed).)|  
  
### Remarks  
 The gallery menu button is displayed as a pop-up menu with an arrow. When the user clicks this button, a gallery of images is displayed. When you construct a gallery menu button, you must specify an image list that contains those images.  
  
## Example  
 The following example demonstrates how to display a gallery of bullets in a menu button:  
  
```  
BOOL CMainFrame::OnShowPopupMenu (CMFCPopupMenu* pMenuPopup)  
{  
    int nBulletIndex = pMenuBar->CommandToIndex (ID_PARA_BULLETS);  
    if (nBulletIndex >= 0)  
    {  
        CMFCToolBarButton* pExButton =  
            pMenuBar->GetButton(nBulletIndex);  
        ASSERT_VALID (pExButton);  
        CMFCRibbonGalleryMenuButton paletteBullet (  
            pExButton->m_nID,  
            pExButton->GetImage (),  
            pExButton->m_strText);  
        InitBulletPalette (&paletteBullet.GetPalette ());  
        pMenuBar->ReplaceButton (ID_PARA_BULLETS, paletteBullet);  
    }  
}  
```  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md) [CMFCToolBarButton](../vs140/CMFCToolBarButton-Class.md) [CMFCToolBarMenuButton](../vs140/CMFCToolBarMenuButton-Class.md) [CMFCRibbonGalleryMenuButton](../vs140/CMFCRibbonGalleryMenuButton-Class.md)  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
##  <a name="cmfcribbongallerymenubutton__copyfrom"></a>  CMFCRibbonGalleryMenuButton::CopyFrom  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void CopyFrom(  
   const CMFCToolBarButton& src  
);  
```  
  
### Parameters  
 [in] `src`  
  
### Remarks  
  
##  <a name="cmfcribbongallerymenubutton__cmfcribbongallerymenubutton"></a>  CMFCRibbonGalleryMenuButton::CMFCRibbonGalleryMenuButton  
 Constructs and initializes a [CMFCRibbonGalleryMenuButton](../vs140/CMFCRibbonGalleryMenuButton-Class.md) object.  
  
```  
CMFCRibbonGalleryMenuButton(  
    UINT uiID,  
    int iImage,  
    LPCTSTR lpszText,  
    CMFCToolBarImages& imagesPalette);  
CMFCRibbonGalleryMenuButton(  
    UINT uiID,  
    int iImage,  
    LPCTSTR lpszText,  
    UINT uiImagesPaletteResID = 0,  
    int cxPaletteImage = 0);  
```  
  
### Parameters  
 `uiID`  
 The command ID of the button. This is the value sent in the                                 **WM_COMMAND** message when the user clicks this button.  
  
 `iImage`  
 The index of the image to display with the gallery menu button. The images are stored in the `imagesPalette` parameter.  
  
 `lpszText`  
 The text to display on the menu button.  
  
 `imagesPalette`  
 Contains the list of images to display on the gallery.  
  
 `uiImagesPaletteResID`  
 The resource ID of the image list for the images to display on the gallery.  
  
 `cxPaletteImage`  
 Specifies the width in pixels of the image to display on the gallery.  
  
### Remarks  
 The gallery menu button is displayed as a pop-up menu that has an arrow. When the user clicks this button, a gallery of images is displayed.  
  
### Example  
 The following example demonstrates how to use the constructor of the `CMFCRibbonGalleryMenuButton` class. This code snippet is part of the [MS Office 2007 Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_MSOffice2007Demo#8](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_MSOffice2007Demo#8)]  
  
##  <a name="cmfcribbongallerymenubutton__createpopupmenu"></a>  CMFCRibbonGalleryMenuButton::CreatePopupMenu  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual CMFCPopupMenu* CreatePopupMenu();  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcribbongallerymenubutton__getpalette"></a>  CMFCRibbonGalleryMenuButton::GetPalette  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CMFCRibbonGallery& GetPalette();  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcribbongallerymenubutton__hasbutton"></a>  CMFCRibbonGalleryMenuButton::HasButton  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL HasButton() const;  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcribbongallerymenubutton__isemptymenuallowed"></a>  CMFCRibbonGalleryMenuButton::IsEmptyMenuAllowed  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL IsEmptyMenuAllowed() const;  
```  
  
### Return Value  
  
### Remarks  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCToolBarMenuButton](../vs140/CMFCToolBarMenuButton-Class.md)   
 [CMFCRibbonGallery Class](../vs140/CMFCRibbonGallery-Class.md)