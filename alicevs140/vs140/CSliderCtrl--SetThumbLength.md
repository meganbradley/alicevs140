---
title: "CSliderCtrl::SetThumbLength"
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
ms.assetid: bbb14b67-61e6-49d1-b5f5-3ab770420b41
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::SetThumbLength
Sets the length of the slider in the current trackbar control.  
  
## Syntax  
  
```  
void SetThumbLength(  
     int nLength  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `nLength`|Length of the slider, in pixels.|  
  
## Remarks  
 This method requires that the trackbar control be set to [TBS_FIXEDLENGTH](http://msdn.microsoft.com/library/windows/desktop/bb760147) style.  
  
 This method sends the [TBM_SETTHUMBLENGTH](http://msdn.microsoft.com/library/windows/desktop/bb760234) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Example  
 The following code example defines the variable, `m_sliderCtrl`, that is used to access the current trackbar control. The example also defines a variable, `thumbLength`, that is used to store the default length of the trackbar control's thumb component. These variables are used in the next example.  
  
 [!CODE [NVC_MFC_CSliderCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSliderCtrl_s1#1)]  
  
## Example  
 The following code example sets the trackbar control's thumb component to twice its default length.  
  
 [!CODE [NVC_MFC_CSliderCtrl_s1#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSliderCtrl_s1#2)]  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TBM_SETTHUMBLENGTH](http://msdn.microsoft.com/library/windows/desktop/bb760234)   
 [CSliderCtrl::GetThumbLength](../vs140/CSliderCtrl--GetThumbLength.md)