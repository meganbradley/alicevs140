---
title: "How to: Provide Hidden Text Support in a Legacy Language Service"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1c1dce9f-bbe2-4fc3-a736-5f78a237f4cc
caps.latest.revision: 23
translation.priority.mt: 
  - de-de
  - ja-jp
---
# How to: Provide Hidden Text Support in a Legacy Language Service
You can create hidden text regions in addition to outline regions. Hidden text regions can be client-controlled or editor-controlled and are used to hide a region of text completely. The editor displays a hidden region as horizontal lines. An example of this is the Script Only view in the HTML editor.  
  
## Procedure  
  
#### To implement a hidden text region  
  
1.  Call `QueryService` for <xref:Microsoft.VisualStudio.TextManager.Interop.SVsTextManager?qualifyHint=False>.  
  
     This returns a pointer to <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager?qualifyHint=False>.  
  
2.  Call <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.GetHiddenTextSession?qualifyHint=False>, passing in a pointer for a given text buffer. This determines whether a hidden text session already exists for the buffer.  
  
3.  If one already exists, then you do not need to create one and a pointer to the existing <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession?qualifyHint=False> object is returned. Use this pointer to enumerate and create hidden text regions. Otherwise, call <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.CreateHiddenTextSession?qualifyHint=False> to create a hidden text session for the buffer.  
  
     A pointer to the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession?qualifyHint=False> object is returned.  
  
    > [!NOTE]
    >  When you call `CreateHiddenTextSession`, you can specify a hidden text client (that is, <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextClient?qualifyHint=False>). The hidden text client notifies you when hidden text or outlining is expanded or collapsed by the user.  
  
4.  Call <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession.AddHiddenRegions?qualifyHint=False> to add one or more new outline regions at a time, specifying the following information in the `reHidReg` (<xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion?qualifyHint=False>) parameter:  
  
    1.  Specify a value of `hrtConcealed` in the `iType` member of the <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion?qualifyHint=False> structure to indicate that you are creating a hidden region, rather than an outline region.  
  
        > [!NOTE]
        >  When concealed regions are hidden, the editor automatically displays lines around the hidden regions to indicate their presence.  
  
    2.  Specify whether the region is client-controlled or editor-controlled in the `dwBehavior` members of the <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion?qualifyHint=False> structure. Your smart outlining implementation can contain a mix of editor- and client-controlled outline and hidden text regions.