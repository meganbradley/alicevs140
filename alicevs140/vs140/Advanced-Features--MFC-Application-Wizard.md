---
title: "Advanced Features, MFC Application Wizard"
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
ms.assetid: 8a6681c5-6576-4b12-841a-6862beee76fa
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Advanced Features, MFC Application Wizard
This topic lists options for additional features for your application, such as Help, printing support, and so on. In each section, specify additional support for these advanced features.  
  
 **Context-sensitive help (HTML)**  
 Generates a set of help files for context-sensitive help, available by using F1 and a Help menu, or by clicking a **Help** button on a dialog box. Help support requires the help compiler. If you do not have the help compiler, you can install it by rerunning Setup.  
  
 See [HTML Help: Context-Sensitive Help for Your Programs](../vs140/HTML-Help--Context-Sensitive-Help-for-Your-Programs.md) and [Help Files (HTML Help)](../vs140/Help-Files--HTML-Help-.md) for more information.  
  
 **Printing and print preview**  
 Generates the code to handle the print, print setup and print preview commands by calling member functions in the [CView Class](../vs140/CView-Class.md) from the MFC library. The wizard also adds commands for these functions to the application's menu. Printing support is available only for applications that specify **Document/view architecture support** in the [Application Type, MFC Application Wizard](../vs140/Application-Type--MFC-Application-Wizard.md) page of the wizard. By default, document/view applications have printing support.  
  
 **Automation**  
 Specifies that the application can handle objects that are implemented in another application, or exposes the application to Automation clients.  
  
 **ActiveX controls**  
 Supports ActiveX controls (default). If you do not select this option and later want to insert ActiveX controls into your project, you must add a call to [AfxEnableControlContainer](../vs140/AfxEnableControlContainer.md) in your application's [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md) member function.  
  
 **MAPI (Messaging API)**  
 Specifies that the application can create, manipulate, transfer, and store mail messages.  
  
 **Windows sockets**  
 Supports Windows sockets, which you can use to write applications that communicate over TCP/IP networks.  
  
 **Active Accessibility**  
 Adds support for [IAccessible](http://msdn.microsoft.com/library/windows/desktop/dd318466) to [CWnd](../vs140/CWnd-Class.md)-derived classes, which you can use to customize the user interface for better interaction with accessibility clients.  
  
 **Common Control Manifest**  
 Enabled by default. Generates an application manifest to enable the Common Control DLL that is included with Microsoft Windows XP and newer operating systems.  
  
 Version 6 of the Common Control DLL does not automatically update the earlier version of the Common Controls that your existing applications use. To use version 6 of the Common Control DLL, you must create an application manifest that directs your application to load the DLL. This Common Control DLL also supports the Windows XP themes.  
  
 An application manifest can also specify other DLLs and versions that your application needs. For more information about application manifests, see [Isolated Applications and Side-by-Side Assemblies](http://msdn.microsoft.com/library/dd408052) in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)].  
  
 **Support Restart Manager**  
 Adds support for the [Windows Restart Manager](http://msdn.microsoft.com/library/windows/desktop/aa373680\(v=vs.85\).aspx). This video shows how to use the Restart Manager from MFC: [How Do I: Use the New Restart Manager?](http://msdn.microsoft.com/vstudio/ee886407).  
  
 **Advanced frame panes**  
 |Option|Description|  
|------------|-----------------|  
|**Explorer docking pane**|Creates a docking pane that resembles the Visual Studio **Solution Explorer** to the left of the main frame window.|  
|**Output docking frame**|Creates a docking pane that resembles the Visual Studio **Output** pane that is located under the main frame window.|  
|**Properties docking pane**|Creates a docking pane that resembles the Visual Studio **Properties** pane to the right of the main frame window.|  
|**Navigation pane**|Creates a docking pane that resembles the Outlook navigation bar and is located to the left of the main frame window.|  
|**Caption bar**|Creates an Office-style caption bar above the main frame window.|  
  
 **Number of files on recent file list**  
 Specifies the number of files to be listed on the most recently used list. The default number is 4.  
  
## See Also  
 [MFC Application Wizard](../vs140/MFC-Application-Wizard.md)