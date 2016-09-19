---
title: "How to: Open Project-Specific Editors"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 83e56d39-c97b-4c6b-86d6-3ffbec97e8d1
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# How to: Open Project-Specific Editors
If an item file being opened by a project is intrinsically bound to the particular editor for that project, the project must open the file by using a project-specific editor. The file cannot be delegated down to the IDE's mechanism for selecting an editor. For example, instead of using a standard bitmap editor, you can use this project-specific editor option to specify a specific bitmap editor that recognizes information in the file that is unique to your project.  
  
 The IDE calls the <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.OpenItem?qualifyHint=False> method when it determines that a file should be opened by a specific project. For more information, see [Displaying Files By Using the Open File Command](../Topic/Displaying%20Files%20By%20Using%20the%20Open%20File%20Command.md). Use the following guidelines to implement the `OpenItem` method to have your project open a file by using a project-specific editor.  
  
### To implement the OpenItem method with a project-specific editor  
  
1.  Call the <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable.FindAndLockDocument?qualifyHint=False> method (RDT_EditLock) to determine whether the file (document data object) is already open.  
  
    > [!NOTE]
    >  For more information about document data and document view objects, see [Document Data and Document View in Custom Editors](../Topic/Document%20Data%20and%20Document%20View%20in%20Custom%20Editors.md).  
  
2.  If the file is already open, resurface the file by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.IsDocumentOpen?qualifyHint=False> method and specifying a value of IDO_ActivateIfOpen for the `grfIDO` parameter.  
  
     If the file is open and the document is owned by a project other than the calling project, a warning will be displayed to the user that the editor being opened is from another project. The file window is then surfaced.  
  
3.  If your text buffer (document data object) is already open and you want to attach another view to it, you are responsible for hooking up that view. The recommended approach to instantiating a view (document view object) from the project, is as follows:  
  
    1.  Call `QueryService` on the <xref:Microsoft.VisualStudio.Shell.Interop.SLocalRegistry?qualifyHint=False> service to get a pointer to the <xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2?qualifyHint=False> interface.  
  
    2.  Call the <xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2.CreateInstance?qualifyHint=False> method to create an instance of the document view class.  
  
4.  Call the <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.CreateDocumentWindow?qualifyHint=False> method, specifying your document view object.  
  
     This method sites the document view object in a document window.  
  
5.  Perform the appropriate calls to either the <xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat.InitNew?qualifyHint=False> or the <xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat.Load?qualifyHint=False> methods.  
  
     At this point, the view should be fully initialized and ready to be opened.  
  
6.  Call the <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.Show?qualifyHint=False> method to show and open the view.  
  
## See Also  
 [Opening and Saving Project Items](../vs140/Opening-and-Saving-Project-Items.md)   
 [How to: Open Standard Editors](../vs140/How-to--Open-Standard-Editors.md)   
 [How to: Open Editors for Open Documents](../Topic/How%20to:%20Open%20Editors%20for%20Open%20Documents.md)