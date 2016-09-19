---
title: "COleControl::IsConvertingVBX"
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
ms.assetid: f2db71e6-be85-467d-8d00-622a9c9118b5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::IsConvertingVBX
Allows specialized loading of an OLE control.  
  
## Syntax  
  
```  
  
BOOL IsConvertingVBX( );  
```  
  
## Return Value  
 Nonzero if the control is being converted; otherwise 0.  
  
## Remarks  
 When converting a form that uses VBX controls to one that uses OLE controls, special loading code for the OLE controls may be required. For example, if you are loading an instance of your OLE control, you might have a call to [PX_Font](../vs140/PX_Font.md) in your `DoPropExchange`:  
  
 [!CODE [NVC_MFCAxCtl#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#3)]  
  
 However, VBX controls did not have a Font object; each font property was saved individually. In this case, you would use `IsConvertingVBX` to distinguish between these two cases:  
  
 [!CODE [NVC_MFCAxCtl#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#4)]  
  
 Another case would be if your VBX control saved proprietary binary data (in its **VBM_SAVEPROPERTY** message handler), and your OLE control saves its binary data in a different format. If you want your OLE control to be backward-compatible with the VBX control, you could read both the old and new formats using the `IsConvertingVBX` function by distinguishing whether the VBX control or the OLE control was being loaded.  
  
 In your control's `DoPropExchange` function, you can check for this condition and if true, execute load code specific to this conversion (such as the previous examples). If the control is not being converted, you can execute normal load code. This ability is only applicable to controls being converted from VBX counterparts.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)