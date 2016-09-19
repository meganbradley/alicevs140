---
title: "CBitmapButton::CBitmapButton"
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
ms.assetid: 15cdfae7-f25e-4abe-8e3b-e435985e86ed
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBitmapButton::CBitmapButton
Creates a `CBitmapButton` object.  
  
## Syntax  
  
```  
  
CBitmapButton( );  
```  
  
## Remarks  
 After creating the C++ `CBitmapButton` object, call [CButton::Create](../vs140/CButton--Create.md) to create the Windows button control and attach it to the `CBitmapButton` object.  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#57](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#57)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CBitmapButton Class](../vs140/CBitmapButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBitmapButton::LoadBitmaps](../vs140/CBitmapButton--LoadBitmaps.md)   
 [CBitmapButton::AutoLoad](../vs140/CBitmapButton--AutoLoad.md)   
 [CBitmapButton::SizeToContent](../vs140/CBitmapButton--SizeToContent.md)   
 [CButton::Create](../vs140/CButton--Create.md)