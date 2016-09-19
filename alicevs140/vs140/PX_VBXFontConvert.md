---
title: "PX_VBXFontConvert"
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
ms.topic: article
ms.assetid: 92a0bcb0-f882-4fac-97d9-16699f83f6ba
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PX_VBXFontConvert
Call this function within your control's `DoPropExchange` member function to initialize a font property by converting a VBX control's font-related properties.  
  
## Syntax  
  
```  
  
      BOOL PX_VBXFontConvert(  
   CPropExchange* pPX,  
   CFontHolder& font   
);  
```  
  
#### Parameters  
 `pPX`  
 Pointer to the [CPropExchange](../vs140/CPropExchange-Class.md) object (typically passed as a parameter to `DoPropExchange`).  
  
 `font`  
 The font property of the OLE control that will contain the converted VBX font-related properties.  
  
## Return Value  
 Nonzero if the exchange was successful; 0 if unsuccessful.  
  
## Remarks  
 This function should be used only by an OLE control that is designed as a direct replacement for a VBX control. When the Visual Basic development environment converts a form containing a VBX control to use the corresponding replacement OLE control, it will call the control's **IDataObject::SetData** function, passing in a property set that contains the VBX control's property data. This operation, in turn, causes the control's `DoPropExchange` function to be invoked. `DoPropExchange` can call `PX_VBXFontConvert` to convert the VBX control's font-related properties (for example, "FontName," "FontSize," and so on) into the corresponding components of the OLE control's font property.  
  
 `PX_VBXFontConvert` should only be called when the control is actually being converted from a VBX form application. For example:  
  
 [!CODE [NVC_MFCActiveXControl#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCActiveXControl#14)]  
[!CODE [NVC_MFCActiveXControl#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCActiveXControl#15)]  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [COleControl::AmbientFont](../vs140/COleControl--AmbientFont.md)   
 [PX_Font](../vs140/PX_Font.md)