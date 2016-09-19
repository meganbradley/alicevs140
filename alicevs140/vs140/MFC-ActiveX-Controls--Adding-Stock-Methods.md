---
title: "MFC ActiveX Controls: Adding Stock Methods"
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
ms.assetid: bc4fad78-cabd-4cc0-a798-464b1a682f0b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC ActiveX Controls: Adding Stock Methods
A stock method differs from a custom method in that it is already implemented by class [COleControl](../vs140/COleControl-Class.md). For example, `COleControl` contains a predefined member function that supports the Refresh method for your control. The dispatch map entry for this stock method is **DISP_STOCKFUNC_REFRESH**.  
  
 `COleControl` supports two stock methods: DoClick and Refresh. Refresh is invoked by the control's user to immediately update the control's appearance; DoClick is invoked to fire the control's Click event.  
  
|Method|Dispatch map entry|Comment|  
|------------|------------------------|-------------|  
|`DoClick`|**DISP_STOCKPROP_DOCLICK( )**|Fires a Click event.|  
|**Refresh**|**DISP_STOCKPROP_REFRESH( )**|Immediately updates the control's appearance.|  
  
##  <a name="_core_adding_a_stock_method_using_classwizard"></a> Adding a Stock Method Using the Add Method Wizard  
 Adding a stock method is simple using the [Add Method Wizard](../vs140/Add-Method-Wizard.md). The following procedure demonstrates adding the Refresh method to a control created using the MFC ActiveX Control Wizard.  
  
#### To add the stock Refresh method using the Add Method Wizard  
  
1.  Load your control's project.  
  
2.  In Class View, expand the library node of your control.  
  
3.  Right-click the interface node for your control (the second node of the library node) to open the shortcut menu.  
  
4.  From the shortcut menu, click **Add** and then click **Add Method**.  
  
     This opens the Add Method Wizard.  
  
5.  In the **Method Name** box, click **Refresh**.  
  
6.  Click **Finish**.  
  
##  <a name="_core_classwizard_changes_for_stock_methods"></a> Add Method Wizard Changes for Stock Methods  
 Because the stock Refresh method is supported by the control's base class, the **Add Method Wizard** does not change the control's class declaration in any way. It adds an entry for the method to the control's dispatch map and to its .IDL file. The following line is added to the control's dispatch map, located in its implementation (.CPP) file:  
  
 [!CODE [NVC_MFC_AxUI#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#16)]  
  
 This makes the Refresh method available to the control's users.  
  
 The following line is added to the control's .IDL file:  
  
 [!CODE [NVC_MFC_AxUI#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxUI#17)]  
  
 This line assigns the Refresh method a specific ID number.  
  
## See Also  
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)