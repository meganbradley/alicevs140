---
title: "Derived Window Classes"
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
ms.assetid: 6f7e437e-fbde-4a06-bfab-72d9dbf05292
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Derived Window Classes
You can create windows directly from [CWnd](../vs140/CWnd-Class.md), or derive new window classes from `CWnd`. This is how you typically create your own custom windows. However, most windows used in a framework program are instead created from one of the `CWnd`-derived frame-window classes supplied by MFC.  
  
## Frame Window Classes  
 [CFrameWnd](../vs140/CFrameWnd-Class.md)  
 Used for SDI frame windows that frame a single document and its view. The frame window is both the main frame window for the application and the frame window for the current document.  
  
 [CMDIFrameWnd](../vs140/CMDIFrameWnd-Class.md)  
 Used as the main frame window for MDI applications. The main frame window is a container for all MDI document windows and shares its menu bar with them. An MDI frame window is a top-level window that appears on the desktop.  
  
 [CMDIChildWnd](../vs140/CMDIChildWnd-Class.md)  
 Used for individual documents opened in an MDI main frame window. Each document and its view are framed by an MDI child frame window contained by the MDI main frame window. An MDI child window looks much like a typical frame window but is contained inside an MDI frame window instead of sitting on the desktop. However, the MDI child window lacks a menu bar of its own and must share the menu bar of the MDI frame window that contains it.  
  
 For more information, see [Frame Windows](../vs140/Frame-Windows.md).  
  
## Other Window Classes Derived from CWnd  
 In addition to frame windows, several other major categories of windows are derived from `CWnd`:  
  
 *Views*  
 Views are created using the `CWnd`-derived class [CView](../vs140/CView-Class.md) (or one of its derived classes). A view is attached to a document and acts as an intermediary between the document and the user. A view is a child window (not an MDI child) that typically fills the client area of an SDI frame window or an MDI child frame window (or that portion of the client area not covered by a toolbar and/or a status bar).  
  
 *Dialog Boxes*  
 Dialog boxes are created using the `CWnd`-derived class [CDialog](../vs140/CDialog-Class.md).  
  
 *Forms*  
 Form views based on dialog-template resources, such as dialog boxes, are created using classes [CFormView](../vs140/CFormView-Class.md), [CRecordView](../vs140/CRecordView-Class.md), or [CDaoRecordView](../vs140/CDaoRecordView-Class.md).  
  
 *Controls*  
 Controls such as buttons, list boxes, and combo boxes are created using other classes derived from `CWnd`. See [Control Topics](../vs140/Controls--MFC-.md).  
  
 *Control Bars*  
 Child windows that contain controls. Examples include toolbars and status bars. See [Control Bars](../vs140/Control-Bars.md).  
  
## Window Class Hierarchy  
 Refer to the [MFC hierarchy chart](../vs140/Hierarchy-Chart.md) in the *MFC Reference*. Views are explained in [Document/View Architecture](../vs140/Document-View-Architecture.md). Dialog boxes are explained in [Dialog Boxes](../vs140/Dialog-Boxes.md).  
  
## Creating Your Own Special-Purpose Window Classes  
 In addition to the window classes provided by the class library, you may need special-purpose child windows. To create such a window, create your own [CWnd](../vs140/CWnd-Class.md)-derived class and make it a child window of a frame or view. Bear in mind that the framework manages the extent of the client area of a document frame window. Most of the client area is managed by a view, but other windows, such as control bars or your own custom windows, may share the space with the view. You may need to interact with the mechanisms in classes [CView](../vs140/CView-Class.md) and [CControlBar](../vs140/CControlBar-Class.md) for positioning child windows in a frame window's client area.  
  
 [Creating Windows](../vs140/Creating-Windows.md) discusses creation of window objects and the windows they manage.  
  
## See Also  
 [Window Objects](../vs140/Window-Objects.md)