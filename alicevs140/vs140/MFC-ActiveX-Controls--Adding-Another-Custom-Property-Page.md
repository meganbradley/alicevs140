---
title: "MFC ActiveX Controls: Adding Another Custom Property Page"
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
ms.assetid: fcf7e119-9f29-41a9-908d-e9b1607e08af
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC ActiveX Controls: Adding Another Custom Property Page
Occasionally, an ActiveX control will have more properties than can reasonably fit on one property page. In this case, you can add property pages to the ActiveX control to display these properties.  
  
 This article discusses adding new property pages to an ActiveX control that already has at least one property page. For more information on adding stock property pages (font, picture, or color), see the article [MFC ActiveX Controls: Using Stock Property Pages](../vs140/MFC-ActiveX-Controls--Using-Stock-Property-Pages.md).  
  
 The following procedures use a sample ActiveX control framework created by the ActiveX Control Wizard. Therefore, the class names and identifiers are unique to this example.  
  
 For more information on using property pages in an ActiveX control, see the following articles:  
  
-   [MFC ActiveX Controls: Property Pages](../vs140/MFC-ActiveX-Controls--Property-Pages.md)  
  
-   [MFC ActiveX Controls: Using Stock Property Pages](../vs140/MFC-ActiveX-Controls--Using-Stock-Property-Pages.md)  
  
    > [!NOTE]
    >  It is strongly recommended that new property pages adhere to the size standard for ActiveX control property pages. The stock picture and color property pages measure 250x62 dialog units (DLU). The standard font property page is 250x110 DLUs. The default property page created by the ActiveX Control Wizard uses the 250x62 DLU standard.  
  
### To insert a new property page template into your project  
  
1.  With your control project open, open Resource View in the project workspace.  
  
2.  Right-click in Resource View to open the shortcut menu and click **Add Resource**.  
  
3.  Expand the **Dialog** node, and select **IDD_OLE_PROPPAGE_SMALL**.  
  
4.  Click `New` to add the resource to your project.  
  
5.  Select the new property page template to refresh the Properties window.  
  
6.  Enter a new value for the **ID** property. This example uses **IDD_PROPPAGE_NEWPAGE**.  
  
7.  Click **Save** on the toolbar.  
  
### To associate the new template with a class  
  
1.  Open Class View.  
  
2.  Right-click in Class View to open the shortcut menu.  
  
3.  From the shortcut menu, click **Add** and then click **Add Class**.  
  
     This opens the [Add Class](../vs140/Add-Class-Dialog-Box.md) dialog box.  
  
4.  Double-click the **MFC Class** template.  
  
5.  In the **Class Name** box in the [MFC Class Wizard](../vs140/MFC-Add-Class-Wizard.md), type a name for the new dialog class. (In this example, `CAddtlPropPage`.)  
  
6.  If you want to change file names, click **Change**. Type in the names for your implementation and header files, or accept the default names.  
  
7.  In the **Base Class** box, select `COlePropertyPage`.  
  
8.  In the **Dialog ID** box, select **IDD_PROPPAGE_NEWPAGE**.  
  
9. Click **Finish** to create the class.  
  
 To allow the control's users access to this new property page, make the following changes to the control's property page IDs macro section (located in the control implementation file):  
  
 [!CODE [NVC_MFC_AxUI#32](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#32)]  
  
 Note that you must increase the second parameter of the `BEGIN_PROPPAGEIDS` macro (the property page count) from 1 to 2.  
  
 You must also modify the control implementation file (.CPP) file to include the header (.H) file of the new property page class.  
  
 The next step involves creating two new string resources that will provide a type name and a caption for the new property page.  
  
#### To add new string resources to a property page  
  
1.  With your control project open, open Resource View.  
  
2.  Double-click the **String Table** folder and then double-click the existing string table resource to which you want to add a string.  
  
     This opens the string table in a window.  
  
3.  Select the blank line at the end of the string table and type the text, or caption, of the string: for example, "Additional Property Page."  
  
     This opens a **String Properties** page showing **Caption** and **ID** boxes. The **Caption** box contains the string you typed.  
  
4.  In the **ID** box, select or type an ID for the string. Press Enter when you finish.  
  
     This example uses **IDS_SAMPLE_ADDPAGE** for the type name of the new property page.  
  
5.  Repeat steps 3 and 4 using **IDS_SAMPLE_ADDPPG_CAPTION** for the ID and "Additional Property Page" for the caption.  
  
6.  In the .CPP file of your new property page class (in this example, `CAddtlPropPage`) modify the `CAddtlPropPage::CAddtlPropPageFactory::UpdateRegistry` so that IDS_SAMPLE_ADDPAGE is passed by [AfxOleRegisterPropertyPageClass](../vs140/AfxOleRegisterPropertyPageClass.md), as in the following example:  
  
     [!CODE [NVC_MFC_AxUI#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#33)]  
  
7.  Modify the constructor of `CAddtlPropPage` so that **IDS_SAMPLE_ADDPPG_CAPTION** is passed to the `COlePropertyPage` constructor, as follows:  
  
     [!CODE [NVC_MFC_AxUI#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#34)]  
  
 After you have made the necessary modifications rebuild your project and use Test Container to test the new property page. See [Testing Properties and Events with Test Container](../vs140/Testing-Properties-and-Events-with-Test-Container.md) for information on how to access the test container.  
  
## See Also  
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)