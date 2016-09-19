---
title: "CMFCRibbonLinkCtrl Class"
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
ms.assetid: 77ae1941-e0ab-4a9d-911e-1752d34c079b
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonLinkCtrl Class
Implements a hyperlink that is positioned on a ribbon. The hyperlink opens a Web page when you click it.  
  
## Syntax  
  
```  
class CMFCRibbonLinkCtrl : public CMFCRibbonButton  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCRibbonLinkCtrl::CMFCRibbonLinkCtrl](#cmfcribbonlinkctrl__cmfcribbonlinkctrl)|Constructs and initializes a `CMFCRibbonLinkCtrl` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCRibbonLinkCtrl::CopyFrom](#cmfcribbonlinkctrl__copyfrom)|(Overrides `CMFCRibbonButton::CopyFrom`.)|  
|[CMFCRibbonLinkCtrl::GetCompactSize](#cmfcribbonlinkctrl__getcompactsize)|(Overrides [CMFCRibbonButton::GetCompactSize](../vs140/CMFCRibbonButton-Class.md#cmfcribbonbutton__getcompactsize).)|  
|[CMFCRibbonLinkCtrl::GetLink](#cmfcribbonlinkctrl__getlink)|Returns the value of the hyperlink.|  
|[CMFCRibbonLinkCtrl::GetRegularSize](#cmfcribbonlinkctrl__getregularsize)|(Overrides [CMFCRibbonButton::GetRegularSize](../vs140/CMFCRibbonButton-Class.md#cmfcribbonbutton__getregularsize).)|  
|[CMFCRibbonLinkCtrl::GetToolTipText](#cmfcribbonlinkctrl__gettooltiptext)|(Overrides [CMFCRibbonButton::GetToolTipText](../vs140/CMFCRibbonButton-Class.md#cmfcribbonbutton__gettooltiptext).)|  
|[CMFCRibbonLinkCtrl::IsDrawTooltipImage](#cmfcribbonlinkctrl__isdrawtooltipimage)|(Overrides `CMFCRibbonButton::IsDrawTooltipImage`.)|  
|[CMFCRibbonLinkCtrl::OnDraw](#cmfcribbonlinkctrl__ondraw)|(Overrides [CMFCRibbonButton::OnDraw](../vs140/CMFCRibbonButton-Class.md#cmfcribbonbutton__ondraw).)|  
|[CMFCRibbonLinkCtrl::OnDrawMenuImage](#cmfcribbonlinkctrl__ondrawmenuimage)|(Overrides [CMFCRibbonBaseElement::OnDrawMenuImage](../vs140/CMFCRibbonBaseElement-Class.md#cmfcribbonbaseelement__ondrawmenuimage).)|  
|[CMFCRibbonLinkCtrl::OnMouseMove](#cmfcribbonlinkctrl__onmousemove)|(Overrides `CMFCRibbonButton::OnMouseMove`.)|  
|[CMFCRibbonLinkCtrl::OnSetIcon](#cmfcribbonlinkctrl__onseticon)||  
|[CMFCRibbonLinkCtrl::OpenLink](#cmfcribbonlinkctrl__openlink)|Opens the Web page specified in the hyperlink.|  
|[CMFCRibbonLinkCtrl::SetLink](#cmfcribbonlinkctrl__setlink)|Sets the value of the hyperlink.|  
  
## Remarks  
 After you create a hyperlink, add it to a panel by calling [CMFCRibbonPanel::Add](../vs140/CMFCRibbonPanel-Class.md#cmfcribbonpanel__add).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md) [CMFCRibbonBaseElement](../vs140/CMFCRibbonBaseElement-Class.md)  
  
 [CMFCRibbonButton](../vs140/CMFCRibbonButton-Class.md) [CMFCRibbonLinkCtrl](../vs140/CMFCRibbonLinkCtrl-Class.md)  
  
## Requirements  
 **Header:** afxRibbonLinkCtrl.h  
  
##  <a name="cmfcribbonlinkctrl__cmfcribbonlinkctrl"></a>  CMFCRibbonLinkCtrl::CMFCRibbonLinkCtrl  
 Constructs and initializes a [CMFCRibbonLinkCtrl](../vs140/CMFCRibbonLinkCtrl-Class.md) object.  
  
```  
CMFCRibbonLinkCtrl(  
    UINT nID,  
    LPCTSTR lpszText,  
    LPCTSTR lpszLink   
);  
```  
  
### Parameters  
 [in] `nID`  
 Specifies the command ID of the command that executes when the link control is clicked.  
  
 [in] `lpszText`  
 Specifies the label to display on the link control.  
  
 [in] `lpszLink`  
 Specifies the hyperlink associated with the link control.  
  
### Example  
 The following example demonstrates how to use the constructor of the `CMFCRibbonLinkCtrl` class. This code snippet is part of the [Ribbon Gadgets sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_RibbonGadgets#1](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonGadgets#1)]  
  
##  <a name="cmfcribbonlinkctrl__copyfrom"></a>  CMFCRibbonLinkCtrl::CopyFrom  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void CopyFrom(  
   const CMFCRibbonBaseElement& src  
);  
```  
  
### Parameters  
 [in] `src`  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__getcompactsize"></a>  CMFCRibbonLinkCtrl::GetCompactSize  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual CSize GetCompactSize(  
   CDC* pDC  
);  
```  
  
### Parameters  
 [in] `pDC`  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__getlink"></a>  CMFCRibbonLinkCtrl::GetLink  
 Returns the value of the hyperlink.  
  
```  
LPCTSTR GetLink() const;  
```  
  
### Return Value  
 The current value of the hyperlink.  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__getregularsize"></a>  CMFCRibbonLinkCtrl::GetRegularSize  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual CSize GetRegularSize(  
   CDC* pDC  
);  
```  
  
### Parameters  
 [in] `pDC`  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__gettooltiptext"></a>  CMFCRibbonLinkCtrl::GetToolTipText  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual CString GetToolTipText() const;  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__ondrawmenuimage"></a>  CMFCRibbonLinkCtrl::OnDrawMenuImage  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL OnDrawMenuImage( CDC*, CRect  
);  
```  
  
### Parameters  
 [in] `CDC*`  
  [in] `CRect`  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__isdrawtooltipimage"></a>  CMFCRibbonLinkCtrl::IsDrawTooltipImage  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL IsDrawTooltipImage() const;  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__ondraw"></a>  CMFCRibbonLinkCtrl::OnDraw  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnDraw(  
   CDC* pDC  
);  
```  
  
### Parameters  
 [in] `pDC`  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__onmousemove"></a>  CMFCRibbonLinkCtrl::OnMouseMove  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnMouseMove(  
   CPoint point  
);  
```  
  
### Parameters  
 [in] `point`  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__onseticon"></a>  CMFCRibbonLinkCtrl::OnSetIcon  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnSetIcon();  
```  
  
### Remarks  
  
##  <a name="cmfcribbonlinkctrl__openlink"></a>  CMFCRibbonLinkCtrl::OpenLink  
 Opens the Web page specified in the hyperlink.  
  
```  
BOOL OpenLink();  
```  
  
### Return Value  
 `TRUE` if the associated Web page was opened successfully; otherwise, `FALSE`.  
  
### Remarks  
 Opens a web page using the hyperlink associated with the `CMFCRibbonLinkCtrl` object.  
  
##  <a name="cmfcribbonlinkctrl__setlink"></a>  CMFCRibbonLinkCtrl::SetLink  
 Sets the value of the hyperlink.  
  
```  
void SetLink(  
    LPCTSTR lpszLink   
);  
```  
  
### Parameters  
 [in] `lpszLink`  
 Specifies the hyperlink text.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)