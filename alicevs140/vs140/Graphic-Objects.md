---
title: "Graphic Objects"
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
ms.assetid: 41963b25-34b7-4343-8446-34ba516b83ca
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Graphic Objects
Windows provides a variety of drawing tools to use in device contexts. It provides pens to draw lines, brushes to fill interiors, and fonts to draw text. MFC provides graphic-object classes equivalent to the drawing tools in Windows. The table below shows the available classes and the equivalent Windows graphics device interface (GDI) handle types.  
  
> [!NOTE]
>  GDI+ is included with Windows XP and is available as a redistributable for Windows NT 4.0  SP6, Windows 2000, Windows 98, and Windows Me. To download the latest redistributable, see  [http://www.microsoft.com/msdownload/platformsdk/sdkupdate/psdkredist.htm](http://www.microsoft.com/msdownload/platformsdk/sdkupdate/psdkredist.htm). For more information, see the GDI+ SDK documentation in MSDN: [http://msdn.microsoft.com/library/default.asp?url=/library/gdicpp/GDIPlus/GDIPlus.asp](http://msdn.microsoft.com/library/default.asp?url=/library/gdicpp/GDIPlus/GDIPlus.asp).  
  
 This article explains the use of these graphic-object classes:  
  
### Classes for Windows GDI Objects  
  
|Class|Windows handle type|  
|-----------|-------------------------|  
|[CPen](../vs140/CPen-Class.md)|`HPEN`|  
|[CBrush](../vs140/CBrush-Class.md)|`HBRUSH`|  
|[CFont](../vs140/CFont-Class.md)|**HFONT**|  
|[CBitmap](../vs140/CBitmap-Class.md)|`HBITMAP`|  
|[CPalette](../vs140/CPalette-Class.md)|`HPALETTE`|  
|[CRgn](../vs140/CRgn-Class.md)|**HRGN**|  
  
> [!NOTE]
>  The class [CImage](../vs140/CImage-Class.md) provides enhanced bitmap support.  
  
 Each graphic-object class in the class library has a constructor that allows you to create graphic objects of that class, which you must then initialize with the appropriate create function, such as `CreatePen`.  
  
 Each graphic-object class in the class library has a cast operator that will cast an MFC object to the associated Windows handle. The resulting handle is valid until the associated object detaches it. Use the object's **Detach** member function to detach the handle.  
  
 The following code casts a `CPen` object to a Windows handle:  
  
 [!CODE [NVC_MFCDocViewSDI#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocViewSDI#5)]  
  
#### To create a graphic object in a device context  
  
1.  Define a graphic object on the stack frame. Initialize the object with the type-specific create function, such as `CreatePen`. Alternatively, initialize the object in the constructor. See the discussion of [one-stage and two-stage creation](../vs140/One-Stage-and-Two-Stage-Construction-of-Objects.md), which provides example code.  
  
2.  [Select the object into the current device context](../vs140/Selecting-a-Graphic-Object-into-a-Device-Context.md), saving the old graphic object that was selected before.  
  
3.  When done with the current graphic object, select the old graphic object back into the device context to restore its state.  
  
4.  Allow the frame-allocated graphic object to be deleted automatically when the scope is exited.  
  
> [!NOTE]
>  If you will be using a graphic object repeatedly, you can allocate it once and select it into a device context each time it is needed. Be sure to delete such an object when you no longer need it.  
  
### What do you want to know more about?  
  
-   [One-stage and two-stage construction of graphic objects](../vs140/One-Stage-and-Two-Stage-Construction-of-Objects.md)  
  
-   [Example of constructing a pen in one and two stages](../vs140/One-Stage-and-Two-Stage-Construction-of-Objects.md)  
  
-   [Selecting a Graphic Object into a Device Context](../vs140/Selecting-a-Graphic-Object-into-a-Device-Context.md)  
  
-   [Device contexts](../vs140/Device-Contexts.md)  
  
-   [CImage limitations with earlier operating systems](../vs140/CImage-Limitations-with-Earlier-Operating-Systems.md)  
  
## See Also  
 [Window Objects](../vs140/Window-Objects.md)