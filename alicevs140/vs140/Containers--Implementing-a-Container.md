---
title: "Containers: Implementing a Container"
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
ms.assetid: af1e2079-619a-4eac-9327-985ad875823a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Containers: Implementing a Container
This article summarizes the procedure for implementing a container and points you to other articles that provide more detailed explanations about implementing containers. It also lists some optional OLE features you may want to implement and the articles describing these features.  
  
#### To prepare your CWinApp-derived class  
  
1.  Initialize the OLE libraries by calling **AfxOleInit** in the `InitInstance` member function.  
  
2.  Call `CDocTemplate::SetContainerInfo` in `InitInstance` to assign the menu and accelerator resources used when an embedded item is activated in-place. For more information on this topic, see [Activation](../vs140/Activation--C---.md).  
  
 These features are provided for you automatically when you use the MFC Application Wizard to create a container application. See [Creating an MFC EXE Program](../vs140/MFC-Application-Wizard.md).  
  
#### To prepare your view class  
  
1.  Keep track of selected items by maintaining a pointer, or list of pointers if you support multiple selection, to the selected items. Your `OnDraw` function must draw all OLE items.  
  
2.  Override `IsSelected` to check whether the item passed to it is currently selected.  
  
3.  Implement an **OnInsertObject** message handler to display the **Insert Object** dialog box.  
  
4.  Implement an `OnSetFocus` message handler to transfer focus from the view to an in-place active OLE embedded item.  
  
5.  Implement an `OnSize` message handler to inform an OLE embedded item that it needs to change its rectangle to reflect the change in size of its containing view.  
  
 Because the implementation of these features varies dramatically from one application to the next, the application wizard provides only a basic implementation. You will likely have to customize these functions to get your application to function properly. For an example of this, see the [CONTAINER](../vs140/Visual-C---Samples.md) sample.  
  
#### To handle embedded and linked items  
  
1.  Derive a class from [COleClientItem](../vs140/COleClientItem-Class.md). Objects of this class represent items that have been embedded in or linked to your OLE document.  
  
2.  Override **OnChange**, `OnChangeItemPosition`, and `OnGetItemPosition`. These functions handle sizing, positioning, and modifying embedded and linked items.  
  
 The application wizard will derive the class for you, but you will likely need to override **OnChange** and the other functions listed with it in step 2 in the preceding procedure. The skeleton implementations need to be customized for most applications, because these functions are implemented differently from one application to the next. For examples of this, see the MFC samples [DRAWCLI](../vs140/Visual-C---Samples.md) and [CONTAINER](../vs140/Visual-C---Samples.md).  
  
 You must add a number of items to the container application's menu structure to support OLE. For more information on these, see [Menus and Resources: Container Additions](../vs140/Menus-and-Resources--Container-Additions.md).  
  
 You may also want to support some of the following features in your container application:  
  
-   In-place activation when editing an embedded item.  
  
     For more information, see [Activation](../vs140/Activation--C---.md).  
  
-   Creation of OLE items by dragging and dropping a selection from a server application.  
  
     For more information, see [Drag and Drop (OLE)](../vs140/Drag-and-Drop--OLE-.md).  
  
-   Links to embedded objects or combination container/server applications.  
  
     For more information, see [Containers: Advanced Features](../vs140/Containers--Advanced-Features.md).  
  
## See Also  
 [Containers](../vs140/Containers.md)   
 [Containers: Client Items](../vs140/Containers--Client-Items.md)