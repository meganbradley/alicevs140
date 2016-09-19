---
title: "Output (Device Context) Classes"
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
ms.assetid: 35fd6435-a38e-42c6-a3fa-cd6f39370fc3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Output (Device Context) Classes
These classes encapsulate the different types of device contexts available in Windows.  
  
 Most of the following classes encapsulate a handle to a Windows device context. A device context is a Windows object that contains information about the drawing attributes of a device such as a display or a printer. All drawing calls are made through a device-context object. Additional classes derived from `CDC` encapsulate specialized device-context functionality, including support for Windows metafiles.  
  
 [CDC](../vs140/CDC-Class.md)  
 The base class for device contexts. Used directly for accessing the whole display and for accessing nondisplay contexts such as printers.  
  
 [CPaintDC](../vs140/CPaintDC-Class.md)  
 A display context used in `OnPaint` member functions of windows. Automatically calls `BeginPaint` on construction and `EndPaint` on destruction.  
  
 [CClientDC](../vs140/CClientDC-Class.md)  
 A display context for client areas of windows. Used, for example, to draw in an immediate response to mouse events.  
  
 [CWindowDC](../vs140/CWindowDC-Class.md)  
 A display context for entire windows, including both the client and nonclient areas.  
  
 [CMetaFileDC](../vs140/CMetaFileDC-Class.md)  
 A device context for Windows metafiles. A Windows metafile contains a sequence of graphics device interface (GDI) commands that can be replayed to create an image. Calls made to the member functions of a `CMetaFileDC` are recorded in a metafile.  
  
## Related Classes  
 [CPoint](../vs140/CPoint-Class.md)  
 Holds coordinate (x, y) pairs.  
  
 [CSize](../vs140/CSize-Class.md)  
 Holds distance, relative positions, or paired values.  
  
 [CRect](../vs140/CRect-Class.md)  
 Holds coordinates of rectangular areas.  
  
 [CRgn](../vs140/CRgn-Class.md)  
 Encapsulates a GDI region for manipulating an elliptical, polygonal, or irregular area within a window. Used in conjunction with the clipping member functions in class `CDC`.  
  
 [CRectTracker](../vs140/CRectTracker-Class.md)  
 Displays and handles the user interface for resizing and moving rectangular objects.  
  
 [CColorDialog](../vs140/CColorDialog-Class.md)  
 Provides a standard dialog box for selecting a color.  
  
 [CFontDialog](../vs140/CFontDialog-Class.md)  
 Provides a standard dialog box for selecting a font.  
  
 [CPrintDialog](../vs140/CPrintDialog-Class.md)  
 Provides a standard dialog box for printing a file.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)