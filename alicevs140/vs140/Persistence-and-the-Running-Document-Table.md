---
title: "Persistence and the Running Document Table"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 27117eae-6c58-4189-a61a-1397a43b5ecf
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Persistence and the Running Document Table
In the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] IDE, projects are completely responsible for managing the persistence of their project items, which they accomplish using the service, <xref:Microsoft.VisualStudio.Shell.Interop.SVsRunningDocumentTable?qualifyHint=False>. Documents are the basic unit of persistence in the Visual Studio environment. Projects coordinate the opening, saving, and renaming of documents with the running document table (RDT), a resource that tracks the state of all open documents.  
  
## Managing Persistence  
 Projects control the environment's persistence service by implementing the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem?qualifyHint=False> interface. While the environment never directly asks a document to persist itself, it asks the owning project (or hierarchy) to save the document. This makes it possible for the project to save its project item data into local files, remote files, a database, a repository, or other medium.  
  
 The global environment maintains the RDT. The environment maintains entries for all open windows and documents in the RDT, which makes it possible for them to receive special notifications, such as when a solution is closed. In addition, the RDT makes it possible for the environment to track their corresponding nodes in **Solution Explorer**. The RDT maintains one record per open, persistable object, including both project files and project-item documents.  
  
## See Also  
 [Running Document Table](../Topic/Running%20Document%20Table.md)   
 [Selection and Currency in the IDE](../Topic/Selection%20and%20Currency%20in%20the%20IDE.md)