---
title: "Example: Implementing a Property Page"
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
ms.assetid: c30b67fe-ce08-4249-ae29-f3060fa8d61e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Example: Implementing a Property Page
This example shows how to build a property page that displays (and allows you to change) properties of the [Document Classes](../vs140/Document-Classes.md) interface. This interface is exposed by documents in Visual Studio's [Common Environment Object Model Examples](assetId:///919cdb58-9f6d-45e6-a0f1-9ca8f6e7051f) (although the property page that you'll create won't care where the objects it manipulates come from as long as they support the correct interface).  
  
 The example is based on the [ATLPages sample](../vs140/Visual-C---Samples.md).  
  
 To complete this example, you will:  
  
-   [Add the ATL property page class](#vcconusing_the_atl_object_wizard) using the Add Class dialog box and the ATL Property Page Wizard.  
  
-   [Edit the dialog resource](#vcconediting_the_dialog_resource) by adding new controls for the interesting properties of the **Document** interface.  
  
-   [Add message handlers](#vcconadding_message_handlers) to keep the property page site informed of changes made by the user.  
  
-   Add some `#import` statements and a typedef in the [Housekeeping](#vcconhousekeeping) section.  
  
-   [Override IPropertyPageImpl::SetObjects](#vcconoverriding_ipropertypageimpl_setobjects) to validate the objects being passed to the property page.  
  
-   [Override IPropertyPageImpl::Activate](#vcconoverriding_ipropertypageimpl_activate) to initialize the property page's interface.  
  
-   [Override IPropertyPageImpl::Apply](#vcconoverride_ipropertypageimpl_apply) to update the object with the latest property values.  
  
-   [Display the property page](#vccontesting_the_property_page) by creating a simple helper object.  
  
-   [Create a macro](#vcconcreating_a_macro) that will test the property page.  
  
##  <a name="vcconusing_the_atl_object_wizard"></a> Adding the ATL Property Page Class  
 First, create a new ATL project for a DLL server called `ATLPages7`. Now use the [ATL Property Page Wizard](../vs140/ATL-Property-Page-Wizard.md) to generate a property page. Give the property page a **Short Name** of **DocProperties** then switch to the **Strings** page to set property-page-specific items as shown in the table below.  
  
|Item|Value|  
|----------|-----------|  
|Title|TextDocument|  
|Doc String|VCUE TextDocument Properties|  
|Helpfile|*<blank\>*|  
  
 The values that you set on this page of the wizard will be returned to the property page container when it calls **IPropertyPage::GetPageInfo**. What happens to the strings after that is dependent on the container, but typically they will be used to identify your page to the user. The Title will usually appear in a tab above your page and the Doc String may be displayed in a status bar or ToolTip (although the standard property frame doesn't use this string at all).  
  
> [!NOTE]
>  The strings that you set here are stored as string resources in your project by the wizard. You can easily edit these strings using the resource editor if you need to change this information after the code for your page has been generated.  
  
 Click **OK** to have the wizard generate your property page.  
  
##  <a name="vcconediting_the_dialog_resource"></a> Editing the Dialog Resource  
 Now that your property page has been generated, you'll need to add a few controls to the dialog resource representing your page. Add an edit box, a static text control, and a check box and set their IDs as shown below:  
  
 ![Editing a dialog resource](../vs140/media/PPGResourceLabeled.gif "PPGResourceLabeled")  
  
 These controls will be used to display the file name of the document and its read-only status.  
  
> [!NOTE]
>  The dialog resource does not include a frame or command buttons, nor does it have the tabbed look that you might have expected. These features are provided by a property page frame such as the one created by calling [OleCreatePropertyFrame](http://msdn.microsoft.com/library/windows/desktop/ms678437).  
  
##  <a name="vcconadding_message_handlers"></a> Adding Message Handlers  
 With the controls in place, you can add message handlers to update the dirty status of the page when the value of either of the controls changes:  
  
 [!CODE [NVC_ATL_Windowing#73](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#73)]  
  
 This code responds to changes made to the edit control or check box by calling [IPropertyPageImpl::SetDirty](../vs140/IPropertyPageImpl--SetDirty.md), which informs the page site that the page has changed. Typically the page site will respond by enabling or disabling an **Apply** button on the property page frame.  
  
> [!NOTE]
>  In your own property pages, you might need to keep track of precisely which properties have been altered by the user so that you can avoid updating properties that haven't been changed. This example implements that code by keeping track of the original property values and comparing them with the current values from the UI when it's time to apply the changes.  
  
##  <a name="vcconhousekeeping"></a> Housekeeping  
 Now add a couple of `#import` statements to DocProperties.h so that the compiler knows about the **Document** interface:  
  
 [!CODE [NVC_ATL_Windowing#74](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#74)]  
  
 You'll also need to refer to the `IPropertyPageImpl` base class; add the following `typedef` to the **CDocProperties** class:  
  
 [!CODE [NVC_ATL_Windowing#75](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#75)]  
  
##  <a name="vcconoverriding_ipropertypageimpl_setobjects"></a> Overriding IPropertyPageImpl::SetObjects  
 The first `IPropertyPageImpl` method that you need to override is [SetObjects](../vs140/IPropertyPageImpl--SetObjects.md). Here you'll add code to check that only a single object has been passed and that it supports the **Document** interface that you're expecting:  
  
 [!CODE [NVC_ATL_Windowing#76](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#76)]  
  
> [!NOTE]
>  It makes sense to support only a single object for this page because you will allow the user to set the file name of the object — only one file can exist at any one location.  
  
##  <a name="vcconoverriding_ipropertypageimpl_activate"></a> Overriding IPropertyPageImpl::Activate  
 The next step is to initialize the property page with the property values of the underlying object when the page is first created.  
  
 In this case you should add the following members to the class since you'll also use the initial property values for comparison when users of the page apply their changes:  
  
 [!CODE [NVC_ATL_Windowing#77](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#77)]  
  
 The base class implementation of the [Activate](../vs140/IPropertyPageImpl--Activate.md) method is responsible for creating the dialog box and its controls, so you can override this method and add your own initialization after calling the base class:  
  
 [!CODE [NVC_ATL_Windowing#78](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#78)]  
  
 This code uses the COM methods of the **Document** interface to get the properties that you're interested in. It then uses the Win32 API wrappers provided by [CDialogImpl](../vs140/CDialogImpl-Class.md) and its base classes to display the property values to the user.  
  
##  <a name="vcconoverride_ipropertypageimpl_apply"></a> Overriding IPropertyPageImpl::Apply  
 When users want to apply their changes to the objects, the property page site will call the [Apply](../vs140/IPropertyPageImpl--Apply.md) method. This is the place to do the reverse of the code in **Activate** — whereas **Activate** took values from the object and pushed them into the controls on the property page, **Apply** takes values from the controls on the property page and pushes them into the object.  
  
 [!CODE [NVC_ATL_Windowing#79](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#79)]  
  
> [!NOTE]
>  The check against [m_bDirty](../vs140/IPropertyPageImpl--m_bDirty.md) at the beginning of this implementation is an initial check to avoid unnecessary updates of the objects if **Apply** is called more than once. There are also checks against each of the property values to ensure that only changes result in a method call to the **Document**.  
  
> [!NOTE]
>  **Document** exposes **FullName** as a read-only property. To update the file name of the document based on changes made to the property page, you have to use the **Save** method to save the file with a different name. Thus, the code in a property page doesn't have to limit itself to getting or setting properties.  
  
##  <a name="vccontesting_the_property_page"></a> Displaying the Property Page  
 To display this page, you need to create a simple helper object. The helper object will provide a method that simplifies the **OleCreatePropertyFrame** API for displaying a single page connected to a single object. This helper will be designed so that it can be used from Visual Basic.  
  
 Use the [Add Class dialog box](../vs140/Add-Class-Dialog-Box.md) and the [ATL Simple Object Wizard](../vs140/ATL-Simple-Object-Wizard.md) to generate a new class and use `Helper` as its short name. Once created, add a method as shown in the table below.  
  
|Item|Value|  
|----------|-----------|  
|Method Name|`ShowPage`|  
|Parameters|`[in] BSTR bstrCaption, [in] BSTR bstrID, [in] IUnknown* pUnk`|  
  
 The `bstrCaption` parameter is the caption to be displayed as the title of the dialog box. The `bstrID` parameter is a string representing either a CLSID or a ProgID of the property page to display. The `pUnk` parameter will be the `IUnknown` pointer of the object whose properties will be configured by the property page.  
  
 Implement the method as shown below:  
  
 [!CODE [NVC_ATL_Windowing#80](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#80)]  
  
##  <a name="vcconcreating_a_macro"></a> Creating a Macro  
 Once you've built the project, you can test the property page and the helper object using a simple macro that you can create and run in the Visual Studio development environment. This macro will create a helper object, then call its **ShowPage** method using the ProgID of the **DocProperties** property page and the **IUnknown** pointer of the document currently active in the Visual Studio editor. The code you need for this macro is shown below:  
  
```  
Imports EnvDTE  
Imports System.Diagnostics  
  
Public Module AtlPages  
  
    Public Sub Test()  
        Dim Helper  
        Helper = CreateObject("ATLPages7.Helper.1")  
  
        On Error Resume Next  
        Helper.ShowPage( _  
            ActiveDocument.Name, _  
            "ATLPages7Lib.DocumentProperties.1", _  
            DTE.ActiveDocument _  
            )  
    End Sub  
  
End Module  
```  
  
 When you run this macro, the property page will be displayed showing the file name and read-only status of the currently active text document. The read-only state of the document only reflects the ability to write to the document in the development environment; it doesn't affect the read-only attribute of the file on disk.  
  
## See Also  
 [Property Pages](../vs140/ATL-COM-Property-Pages.md)   
 [ATLPages Sample](../vs140/Visual-C---Samples.md)