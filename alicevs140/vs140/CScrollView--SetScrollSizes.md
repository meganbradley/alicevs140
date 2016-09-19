---
title: "CScrollView::SetScrollSizes"
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
ms.assetid: f07e1903-80d3-4162-937a-5f12b75f671a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollView::SetScrollSizes
Call `SetScrollSizes` when the view is about to be updated.  
  
## Syntax  
  
```  
  
      void SetScrollSizes(  
   int nMapMode,  
   SIZE sizeTotal,  
   const SIZE& sizePage = sizeDefault,  
   const SIZE& sizeLine = sizeDefault   
);  
```  
  
#### Parameters  
 `nMapMode`  
 The mapping mode to set for this view. Possible values include:  
  
|Mapping Mode|Logical Unit|Positive y-axis Extends...|  
|------------------|------------------|---------------------------------|  
|`MM_TEXT`|1 pixel|Downward|  
|`MM_HIMETRIC`|0.01 mm|Upward|  
|`MM_TWIPS`|1/1440 in|Upward|  
|`MM_HIENGLISH`|0.001 in|Upward|  
|`MM_LOMETRIC`|0.1 mm|Upward|  
|`MM_LOENGLISH`|0.01 in|Upward|  
  
 All of these modes are defined by Windows. Two standard mapping modes, `MM_ISOTROPIC` and `MM_ANISOTROPIC`, are not used for `CScrollView`. The class library provides the `SetScaleToFitSize` member function for scaling the view to window size. Column three in the table above describes the coordinate orientation.  
  
 `sizeTotal`  
 The total size of the scroll view. The **cx** member contains the horizontal extent. The **cy** member contains the vertical extent. Sizes are in logical units. Both **cx** and **cy** must be greater than or equal to 0.  
  
 `sizePage`  
 The horizontal and vertical amounts to scroll in each direction in response to a mouse click in a scroll-bar shaft. The **cx** member contains the horizontal amount. The **cy** member contains the vertical amount.  
  
 `sizeLine`  
 The horizontal and vertical amounts to scroll in each direction in response to a mouse click in a scroll arrow. The **cx** member contains the horizontal amount. The **cy** member contains the vertical amount.  
  
## Remarks  
 Call it in your override of the `OnUpdate` member function to adjust scrolling characteristics when, for example, the document is initially displayed or when it changes size.  
  
 You will typically obtain size information from the view's associated document by calling a document member function, perhaps called `GetMyDocSize`, that you supply with your derived document class. The following code shows this approach:  
  
 [!CODE [NVC_MFCDocView#166](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#166)]  
  
 Alternatively, you might sometimes need to set a fixed size, as in the following code:  
  
 [!CODE [NVC_MFCDocView#167](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#167)]  
  
 You must set the mapping mode to any of the Windows mapping modes except `MM_ISOTROPIC` or `MM_ANISOTROPIC`. If you want to use an unconstrained mapping mode, call the `SetScaleToFitSize` member function instead of `SetScrollSizes`.  
  
## Example  
 [!CODE [NVC_MFCDocView#168](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#168)]  
  
 [!CODE [NVC_MFCDocView#169](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#169)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollView Class](../vs140/CScrollView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollView::SetScaleToFitSize](../vs140/CScrollView--SetScaleToFitSize.md)   
 [CScrollView::GetDeviceScrollSizes](../vs140/CScrollView--GetDeviceScrollSizes.md)   
 [CScrollView::GetTotalSize](../vs140/CScrollView--GetTotalSize.md)