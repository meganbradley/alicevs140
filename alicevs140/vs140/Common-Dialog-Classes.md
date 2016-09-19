---
title: "Common Dialog Classes"
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
ms.assetid: 5c4f6443-896c-4b05-a7df-8169fdadc71d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Common Dialog Classes
In addition to class [CDialog](../vs140/CDialog-Class.md), MFC supplies several classes derived from `CDialog` that encapsulate commonly used dialog boxes, as shown in the following table. The dialog boxes encapsulated are called the "common dialog boxes" and are part of the Windows common dialog library (COMMDLG.DLL). The dialog-template resources and code for these classes are provided in the Windows common dialog boxes that are part of Windows versions 3.1 and later.  
  
### Common Dialog Classes  
  
|Derived dialog class|Purpose|  
|--------------------------|-------------|  
|[CColorDialog](../vs140/CColorDialog-Class.md)|Lets user select colors.|  
|[CFileDialog](../vs140/CFileDialog-Class.md)|Lets user select a filename to open or to save.|  
|[CFindReplaceDialog](../vs140/CFindReplaceDialog-Class.md)|Lets user initiate a find or replace operation in a text file.|  
|[CFontDialog](../vs140/CFontDialog-Class.md)|Lets user specify a font.|  
|[CPrintDialog](../vs140/CPrintDialog-Class.md)|Lets user specify information for a print job.|  
|[CPrintDialogEx](../vs140/CPrintDialogEx-Class.md)|Windows 2000 print property sheet.|  
  
 For more information about the common dialog classes, see the individual class names in the *MFC Reference*. MFC also supplies a number of standard dialog classes used for OLE. For information about these classes, see the base class, [COleDialog](../vs140/COleDialog-Class.md), in the *MFC Reference*.  
  
 Three other classes in MFC have dialog-like characteristics. For information about classes [CFormView](../vs140/CFormView-Class.md), [CRecordView](../vs140/CRecordView-Class.md), and [CDaoRecordView](../vs140/CDaoRecordView-Class.md), see the classes in the *MFC Reference*. For information about class [CDialogBar](../vs140/CDialogBar-Class.md), see [Dialog Bars](../vs140/Dialog-Bars.md).  
  
## See Also  
 [Dialog Boxes](../vs140/Dialog-Boxes.md)   
 [Life Cycle of a Dialog Box](../vs140/Life-Cycle-of-a-Dialog-Box.md)   
 [Dialog Boxes in OLE](../vs140/Dialog-Boxes-in-OLE.md)