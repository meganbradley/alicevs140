---
title: "&lt;PAVE OVER&gt; Displaying F1 Help for a Dialog Box or Menu Option"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 65b39a02-d1ec-465c-9528-4c9d867a7be6
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; Displaying F1 Help for a Dialog Box or Menu Option
When an MFC application is enabled for context sensitive help in HTMLHelp format, you can provide for the display of a topic when a user presses F1 on a menu option or on a dialog box.  
  
### To manually make the HTML Help viewer display  
  
1.  Assuming a dialog box with an ID of IDD_MYDLG, add the following alias to the project's .hhp file: **HIDD_MYDLG = HID_APP_MYDLG.htm**.  
  
2.  Add the following to hlp\afxcore.htm:  
  
    ```  
    <OBJECT type="application/x-oleobject" classid="clsid:1e2a7bd0-dab9-11d0-b93a-00c04fc99f9e" VIEWASTEXT>  
    <param name="New HTML file" value="hid_app_mydlg.htm">  
    <param name="New HTML title" value="MyDlg command (Help menu)">  
    </OBJECT>  
    <P>Help text goes here.</P>  
    ```  
  
 The same procedure will work if the ID is that of a menu option.  
  
## See Also  
 [HTML Help: Context-Sensitive Help for Your Programs](../vs140/HTML-Help--Context-Sensitive-Help-for-Your-Programs.md)   
 [<PAVE OVER\> Displaying Context-Sensitive Help](../vs140/-PAVE-OVER--Displaying-Context-Sensitive-Help.md)   
 [CWinApp::EnableHtmlHelp](../vs140/CWinApp--EnableHtmlHelp.md)   
 [CWnd::HtmlHelp](../vs140/CWnd--HtmlHelp.md)   
 [CWinApp::HtmlHelp](../vs140/CWinApp--HtmlHelp.md)