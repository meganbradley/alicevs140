---
title: "Persistence of OLE Controls"
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
ms.assetid: 64f8dc80-f110-41af-b3ea-14948f6bfdf7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Persistence of OLE Controls
One capability of OLE controls is property persistence (or serialization), which allows the OLE control to read or write property values to and from a file or stream. A container application can use serialization to store a control's property values even after the application has destroyed the control. The property values of the OLE control can then be read from the file or stream when a new instance of the control is created at a later time.  
  
### Persistence of OLE Controls  
  
|||  
|-|-|  
|[PX_Blob](../vs140/PX_Blob.md)|Exchanges a control property that stores binary large object (BLOB) data.|  
|[PX_Bool](../vs140/PX_Bool.md)|Exchanges a control property of type **BOOL**.|  
|[PX_Color](../vs140/PX_Color.md)|Exchanges a color property of a control.|  
|[PX_Currency](../vs140/PX_Currency.md)|Exchanges a control property of type **CY**.|  
|[PX_DataPath](../vs140/PX_DataPath.md)|Exchanges a control property of type `CDataPathProperty`.|  
|[PX_Double](../vs140/PX_Double.md)|Exchanges a control property of type **double**.|  
|[PX_Font](../vs140/PX_Font.md)|Exchanges a font property of a control.|  
|[PX_Float](../vs140/PX_Float.md)|Exchanges a control property of type **float**.|  
|[PX_IUnknown](../vs140/PX_IUnknown.md)|Exchanges a control property of undefined type.|  
|[PX_Long](../vs140/PX_Long.md)|Exchanges a control property of type **long**.|  
|[PX_Picture](../vs140/PX_Picture.md)|Exchanges a picture property of a control.|  
|[PX_Short](../vs140/PX_Short.md)|Exchanges a control property of type **short**.|  
|[PX_ULong](../vs140/PX_ULong.md)|Exchanges a control property of type **ULONG**.|  
|[PX_UShort](../vs140/PX_UShort.md)|Exchanges a control property of type **USHORT**.|  
|[PX_String](../vs140/PX_String.md)|Exchanges a character string control property.|  
|[PX_VBXFontConvert](../vs140/PX_VBXFontConvert.md)|Exchanges a VBX control's font-related properties into an OLE control font property.|  
  
 In addition, the `AfxOleTypeMatchGuid` global function is provided to test for a match between a `TYPEDESC` and a given GUID.  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)