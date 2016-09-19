---
title: "MFC ActiveX Controls: Adding Custom Methods"
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
ms.assetid: 8f8dc344-44a0-4021-8db5-4cdd3d700e18
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC ActiveX Controls: Adding Custom Methods
Custom methods differ from stock methods in that they are not already implemented by `COleControl`. You must supply the implementation for each custom method you add to your control.  
  
 An ActiveX control user can call a custom method at any time to perform control-specific actions. The dispatch map entry for custom methods is of the form `DISP_FUNCTION`.  
  
##  <a name="_core_adding_a_custom_method_with_classwizard"></a> Adding a Custom Method With the Add Method Wizard  
 The following procedure demonstrates adding the custom method PtInCircle to an ActiveX control's skeleton code. PtInCircle determines whether the coordinates passed to the control are inside or outside the circle. This same procedure can also be used to add other custom methods. Substitute your custom method name and its parameters for the PtInCircle method name and parameters.  
  
> [!NOTE]
>  This example uses the `InCircle` function from the article Events. For more information on this function, see the article [MFC ActiveX Controls: Adding Custom Events to an ActiveX Control](../vs140/MFC-ActiveX-Controls--Adding-Custom-Events.md).  
  
#### To add the PtInCircle custom method using the Add Method Wizard  
  
1.  Load the control's project.  
  
2.  In Class View, expand the library node of your control.  
  
3.  Right-click the interface node for your control (the second node of the library node) to open the shortcut menu.  
  
4.  From the shortcut menu, click **Add** and then click **Add Method**.  
  
     This opens the Add Method Wizard.  
  
5.  In the **Method Name** box, type `PtInCircle`.  
  
6.  In the **Internal Name** box, type the name of the method's internal function or use the default value (in this case, `PtInCircle`).  
  
7.  In the **Return Type** box, click **VARIANT_BOOL** for the method's return type.  
  
8.  Using the **Parameter Type** and **Parameter Name** controls, add a parameter called `xCoord` (type **OLE_XPOS_PIXELS**).  
  
9. Using the **Parameter Type** and **Parameter Name** controls, add a parameter called `yCoord` (type **OLE_YPOS_PIXELS**).  
  
10. Click **Finish**.  
  
##  <a name="_core_classwizard_changes_for_custom_methods"></a> Add Method Wizard Changes for Custom Methods  
 When you add a custom method, the Add Method Wizard makes some changes to the control class header (.H) and implementation (.CPP) files. The following line is added to the dispatch map declaration in the control class header (.H) file:  
  
 [!CODE [NVC_MFC_AxUI#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#18)]  
  
 This code declares a dispatch method handler called `PtInCircle`. This function can be called by the control user using the external name PtInCircle.  
  
 The following line is added to the control's .IDL file:  
  
 [!CODE [NVC_MFC_AxUI#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#19)]  
  
 This line assigns the PtInCircle method a specific ID number, the method's position in the Add Method Wizard methods and properties list. Because the Add Method Wizard was used to add the custom method, the entry for it was added automatically to the project's .IDL file.  
  
 In addition, the following line, located in the implementation (.CPP) file of the control class, is added to the control's dispatch map:  
  
 [!CODE [NVC_MFC_AxUI#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#20)]  
  
 The `DISP_FUNCTION` macro maps the method PtInCircle to the control's handler function, `PtInCircle`, declares the return type to be **VARIANT_BOOL**, and declares two parameters of type **VTS_XPOS_PIXELS** and **VTS_YPOSPIXELS** to be passed to `PtInCircle`.  
  
 Finally, the Add Method Wizard adds the stub function `CSampleCtrl::PtInCircle` to the bottom of the control's implementation (.CPP) file. For `PtInCircle` to function as stated previously, it must be modified as follows:  
  
 [!CODE [NVC_MFC_AxUI#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#21)]  
  
## See Also  
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)   
 [Class View and Object Browser Icons](../vs140/Class-View-and-Object-Browser-Icons.md)