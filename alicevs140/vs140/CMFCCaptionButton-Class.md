---
title: "CMFCCaptionButton Class"
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
ms.assetid: c5774b38-c0dd-414a-9ede-3b2f78f233ec
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCaptionButton Class
The `CMFCCaptionButton` class implements a button that is displayed on the caption bar for a docking pane or a mini-frame window. Typically, the framework creates caption buttons automatically.  
  
## Syntax  
  
```  
class CMFCCaptionButton : public CObject  
```  
  
## Members  
  
### Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCCaptionButton::CMFCCaptionButton](#cmfccaptionbutton__cmfccaptionbutton)|Constructs a CMFCCaptionButton object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[GetHit](#cmfccaptionbutton__gethit)|Returns the command represented by the button.|  
|[GetIconID](#cmfccaptionbutton__geticonid)|Returns the image ID associated with the button.|  
|[GetRect](#cmfccaptionbutton__getrect)|Returns the rectangle occupied by the button.|  
|[GetSize](#cmfccaptionbutton__getsize)|Returns the width and height of the button.|  
|[IsMiniFrameButton](#cmfccaptionbutton__isminiframebutton)|Indicates whether the title bar height is set to mini size.|  
|[Move](#cmfccaptionbutton__move)|Sets the button draw location and window show state.|  
|[OnDraw](#cmfccaptionbutton__ondraw)|Draws the caption button.|  
|[SetMiniFrameButton](#cmfccaptionbutton__setminiframebutton)|Sets the mini size of the title bar.|  
  
## Remarks  
 You can derive a class from [CPaneFrameWnd](../vs140/CPaneFrameWnd-Class.md) and use the protected method, `AddButton`, to add caption buttons to a mini frame window.  
  
 CPaneFrameWnd.h defines command IDs for two types of caption buttons:  
  
-   `AFX_CAPTION_BTN_PIN`, which displays a pin button when the docking pane supports auto-hide mode.  
  
-   `AFX_CAPTION_BTN_CLOSE`, which displays a **Close** button when the pane can be closed or hidden.  
  
## Example  
 The following example demonstrates how to construct a `CMFCCaptionButton` object and set the mini size of the title bar.  
  
 [!CODE [NVC_MFC_RibbonApp#43](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#43)]  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CMFCCaptionButton](../vs140/CMFCCaptionButton-Class.md)  
  
## Requirements  
 **Header:** afxcaptionbutton.h  
  
##  <a name="cmfccaptionbutton__cmfccaptionbutton"></a>  CMFCCaptionButton::CMFCCaptionButton  
 Constructs a `CMFCCaptionButton` object.  
  
```  
CMFCCaptionButton();  
CMFCCaptionButton(  
   UINT nHit,  
   BOOL bLeftAlign = FALSE  
);  
```  
  
### Parameters  
 [in] `nHit`  
 The command associated with the button.  
  
 [in] `bLeftAlign`  
 Specifies whether the button is aligned to the left.  
  
 The following table lists possible values for the `nHit` parameter.  
  
|Value|Command|  
|-----------|-------------|  
|`AFX_HTCLOSE`|Close button.|  
|`HTMINBUTTON`|Minimize button.|  
|`HTMAXBUTTON`|Maximize button.|  
|`AFX_HTLEFTBUTTON`|Left arrow button.|  
|`AFX_HTRIGHTBUTTON`|Right arrow button.|  
|`AFX_HTMENU`|Down arrow menu button.|  
|`HTNOWHERE`|The default value; represents no command.|  
  
### Remarks  
 By default, caption buttons are not associated with a command.  
  
 Caption buttons are aligned either on the right or left.  
  
##  <a name="cmfccaptionbutton__gethit"></a>  CMFCCaptionButton::GetHit  
 Returns the command represented by the button.  
  
```  
UINT GetHit() const;  
```  
  
### Return Value  
 The command represented by the button.  
  
 The following table lists possible return values.  
  
|Value|Command|  
|-----------|-------------|  
|`AFX_HTCLOSE`|Close button.|  
|`HTMINBUTTON`|Minimize button.|  
|`HTMAXBUTTON`|Maximize button.|  
|`AFX_HTLEFTBUTTON`|Left arrow button.|  
|`AFX_HTRIGHTBUTTON`|Right arrow button.|  
|`AFX_HTMENU`|Down arrow menu button.|  
|`HTNOWHERE`|The default value; represents no command.|  
  
##  <a name="cmfccaptionbutton__geticonid"></a>  CMFCCaptionButton::GetIconID  
 Returns the image ID associated with the button.  
  
```  
virtual CMenuImages::IMAGES_IDS GetIconID(  
   BOOL bHorz,  
   BOOL bMaximized = FALSE  
) const;  
```  
  
### Parameters  
 [in] `bHorz`  
 `TRUE` for left or right arrow image IDs; `FALSE` for up or down arrow image IDs.  
  
 [in] `bMaximized`  
 `TRUE` for a maximize image ID; `FALSE` for a minimize image ID.  
  
### Return Value  
 The image ID.  
  
### Remarks  
 The parameters specify image IDs for minimize or maximize caption buttons.  
  
##  <a name="cmfccaptionbutton__getrect"></a>  CMFCCaptionButton::GetRect  
 Returns the rectangle occupied by the button.  
  
```  
virtual CRect GetRect() const;  
```  
  
### Return Value  
 The rectangle that represents the location of the button.  
  
### Remarks  
 If you cannot see the button, the size returned is 0.  
  
##  <a name="cmfccaptionbutton__getsize"></a>  CMFCCaptionButton::GetSize  
 Returns the width and height of the button.  
  
```  
static CSize GetSize();  
```  
  
### Return Value  
 The outer dimensions of the button.  
  
### Remarks  
 The size returned includes button margin and border.  
  
##  <a name="cmfccaptionbutton__isminiframebutton"></a>  CMFCCaptionButton::IsMiniFrameButton  
 Indicates whether the title bar height is set to mini size.  
  
```  
BOOL IsMiniFrameButton() const;  
```  
  
### Return Value  
 `TRUE` if the caption is set to mini size; otherwise `FALSE`.  
  
### Remarks  
  
##  <a name="cmfccaptionbutton__move"></a>  CMFCCaptionButton::Move  
 Sets the button draw location and window show state.  
  
```  
void Move(  
   const CPoint& ptTo,  
   BOOL bHide = FALSE  
);  
```  
  
### Parameters  
 [in] `ptTo`  
 The new location.  
  
 [in] `bHide`  
 Whether to show the button.  
  
##  <a name="cmfccaptionbutton__ondraw"></a>  CMFCCaptionButton::OnDraw  
 Draws the caption button.  
  
```  
virtual void OnDraw(  
   CDC* pDC,  
   BOOL bActive,  
   BOOL bHorz = TRUE,  
   BOOL bMaximized = TRUE,  
   BOOL bDisabled = FALSE  
);  
```  
  
### Parameters  
 [in] `pDC`  
 Pointer to a device context for the button.  
  
 [in] `bActive`  
 Whether to draw an active button image.  
  
 [in] `bHorz`  
 Reserved for use in a derived class.  
  
 [in] `bMaximized`  
 Whether to draw a maximized button image.  
  
 [in] `bDisabled`  
 Whether to draw an enabled button image.  
  
### Remarks  
 The `bMaximized` parameter is used when the button is a maximize or minimize button.  
  
##  <a name="cmfccaptionbutton__setminiframebutton"></a>  CMFCCaptionButton::SetMiniFrameButton  
 Sets the mini size of the title bar.  
  
```  
void SetMiniFramebutton(  
   BOOL bSet = TRUE  
);  
```  
  
### Parameters  
 [in] `bSet`  
 `TRUE` for mini title bar height; `FALSE` for default title bar height.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CPaneFrameWnd](../vs140/CPaneFrameWnd-Class.md)   
 [CMFCDockablePane](../vs140/CDockablePane-Class.md)