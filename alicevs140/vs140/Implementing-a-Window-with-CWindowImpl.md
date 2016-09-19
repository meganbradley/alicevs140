---
title: "Implementing a Window with CWindowImpl"
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
ms.assetid: 3fc40550-f1d6-4702-8b7c-4cf682b6a855
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implementing a Window with CWindowImpl
To implement a window, derive a class from `CWindowImpl`. In your derived class, declare a message map and the message handler functions. You can now use your class in three different ways:  
  
-   [Create a window based on a new Windows class](#_atl_creating_a_window_based_on_a_new_windows_class)  
  
-   [Superclass an existing Windows class](#_atl_superclassing_an_existing_windows_class)  
  
-   [Subclass an existing window](#_atl_subclassing_an_existing_window)  
  
##  <a name="_atl_creating_a_window_based_on_a_new_windows_class"></a> Creating a Window Based on a New Windows Class  
 `CWindowImpl` contains the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) macro to declare Windows class information. This macro implements the `GetWndClassInfo` function, which uses [CWndClassInfo](../vs140/CWndClassInfo-Class.md) to define the information of a new Windows class. When `CWindowImpl::Create` is called, this Windows class is registered and a new window is created.  
  
> [!NOTE]
>  `CWindowImpl` passes **NULL** to the `DECLARE_WND_CLASS` macro, which means ATL will generate a Windows class name. To specify your own name, pass a string to `DECLARE_WND_CLASS` in your `CWindowImpl`-derived class.  
  
## Example  
 Following is an example of a class that implements a window based on a new Windows class:  
  
 [!CODE [NVC_ATL_Windowing#64](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#64)]  
  
 To create a window, create an instance of `CMyWindow` and then call the **Create** method.  
  
> [!NOTE]
>  To override the default Windows class information, implement the `GetWndClassInfo` method in your derived class by setting the `CWndClassInfo` members to the appropriate values.  
  
##  <a name="_atl_superclassing_an_existing_windows_class"></a> Superclassing an Existing Windows Class  
 The [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro allows you to create a window that superclasses an existing Windows class. Specify this macro in your `CWindowImpl`-derived class. Like any other ATL window, messages are handled by a message map.  
  
 When you use `DECLARE_WND_SUPERCLASS`, a new Windows class will be registered. This new class will be the same as the existing class you specify, but will replace the window procedure with `CWindowImpl::WindowProc` (or with your function that overrides this method).  
  
## Example  
 Following is an example of a class that superclasses the standard Edit class:  
  
 [!CODE [NVC_ATL_Windowing#65](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#65)]  
  
 To create the superclassed Edit window, create an instance of `CMyEdit` and then call the **Create** method.  
  
##  <a name="_atl_subclassing_an_existing_window"></a> Subclassing an Existing Window  
 To subclass an existing window, derive a class from `CWindowImpl` and declare a message map, as in the two previous cases. Note, however, that you do not specify any Windows class information, since you will subclass an already existing window.  
  
 Instead of calling **Create**, call `SubclassWindow` and pass it the handle to the existing window you want to subclass. Once the window is subclassed, it will use `CWindowImpl::WindowProc` (or your function that overrides this method) to direct messages to the message map. To detach a subclassed window from your object, call `UnsubclassWindow`. The window's original window procedure will then be restored.  
  
## See Also  
 [Implementing a Window](../vs140/Implementing-a-Window.md)