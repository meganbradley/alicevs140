---
title: "Rebar Controls and Bands"
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
ms.assetid: b647e7a5-9ea7-48b1-8e5f-096d104748f0
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Rebar Controls and Bands
The main purpose of a rebar control is to act as a container for child windows, common dialog controls, menus, toolbars, and so on. This containment is supported by the concept of a "band." Each rebar band can contain any combination of a gripper bar, a bitmap, a text label, and a child window.  
  
 Class `CReBarCtrl` has many member functions that you can use to retrieve, and manipulate, information for a specific rebar band:  
  
-   [GetBandCount](../vs140/CReBarCtrl--GetBandCount.md) Retrieves the number of current bands in the rebar control.  
  
-   [GetBandInfo](../vs140/CReBarCtrl--GetBandInfo.md) Initializes a **REBARBANDINFO** structure with information from the specified band. There is a corresponding [SetBandInfo](../vs140/CReBarCtrl--SetBandInfo.md) member function.  
  
-   [GetRect](../vs140/CReBarCtrl--GetRect.md) Retrieves the bounding rectangle of a specified band.  
  
-   [GetRowCount](../vs140/CReBarCtrl--GetRowCount.md) Retrieves the number of band rows in a rebar control.  
  
-   [IDToIndex](../vs140/CReBarCtrl--IDToIndex.md) Retrieves the index of a specified band.  
  
-   [GetBandBorders](../vs140/CReBarCtrl--GetBandBorders.md) Retrieves the borders of a band.  
  
 In addition to manipulation, several member functions are provided that allow you to operate on specific rebar bands.  
  
 [InsertBand](../vs140/CReBarCtrl--InsertBand.md) and [DeleteBand](../vs140/CReBarCtrl--DeleteBand.md) add and remove rebar bands. [MinimizeBand](../vs140/CReBarCtrl--MinimizeBand.md) and [MaximizeBand](../vs140/CReBarCtrl--MaximizeBand.md) affect the current size of a specific rebar band. [MoveBand](../vs140/CReBarCtrl--MoveBand.md) changes the index of a specific rebar band. [ShowBand](../vs140/CReBarCtrl--ShowBand.md) shows or hides a rebar band from the user.  
  
 The following example demonstrates adding a toolbar band (`m_wndToolBar`) to an existing rebar control (`m_wndReBar`). The band is described by initializing the `rbi` structure and then calling the `InsertBand` member function:  
  
 [!CODE [NVC_MFCControlLadenDialog#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#27)]  
  
## See Also  
 [Using CReBarCtrl](../vs140/Using-CReBarCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)