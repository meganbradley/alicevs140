---
title: "CDateTimeCtrl::SetMonthCalFont"
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
ms.assetid: aec0494a-040b-4a11-98ea-2992820c3575
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::SetMonthCalFont
Sets the font that the date and time picker control's child month calendar control will use.  
  
## Syntax  
  
```  
  
      void SetMonthCalFont(  
   HFONT hFont,  
   BOOL bRedraw = TRUE   
);  
```  
  
#### Parameters  
 `hFont`  
 Handle to the font that will be set.  
  
 `bRedraw`  
 Specifies whether the control should be redrawn immediately upon setting the font. Setting this parameter to **TRUE** causes the control to redraw itself.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [DTM_SETMCFONT](http://msdn.microsoft.com/library/windows/desktop/bb761775), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CDateTimeCtrl#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl#7)]  
  
> [!NOTE]
>  If you use this code, you'll want to make a member of your `CDialog`-derived class called `m_MonthFont` of type **CFont**.  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDateTimeCtrl::GetMonthCalFont](../vs140/CDateTimeCtrl--GetMonthCalFont.md)