---
title: "How to: Debug a ClickOnce Application with Restricted Permissions"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-deployment
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6991ea91-5253-451b-923d-22273a3d38b1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Debug a ClickOnce Application with Restricted Permissions
As a developer, you most likely are running your development computer with Full Trust permissions, so you will not see the same security exceptions when debugging a ClickOnce application that the end user may see when running it with restricted permissions.  
  
 In order to catch these exceptions, you need to debug the application with the same permissions as the end user. Debugging with restricted permissions can be enabled on the **Security** page of the **Project Designer**.  
  
 In addition, when you develop applications that call Web services, those Web services often reside on your development computer. Once deployed, the end user will access those Web services from a different URL. In order to emulate the end user experience during debugging, you can specify a URL and the debugger will treat the Web services as if they were being called from that URL.  
  
### To enable debugging with restricted permissions  
  
1.  With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.  
  
2.  In the **Project Designer**, click the **Security** tab.  
  
3.  Select the **Enable ClickOnce Security Setting** check box, and then click the **This is a partial trust application** option button.  
  
4.  Click the **Advanced** button.  
  
5.  Select the **Debug this application with the selected permission set** check box, and then click **OK**.  
  
     When you debug the application, any attempts to access a permission that isn't part of the permission set will raise a security exception.  
  
### To specify a URL for debugging  
  
1.  With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.  
  
2.  In the **Project Designer**, click the **Security** tab.  
  
3.  Select the **Enable ClickOnce Security Setting** check box, and then click the **This is a partial trust application** option button.  
  
4.  Click the **Advanced** button.  
  
5.  Select the **Debug this application with the selected permission set** check box, and then click **OK**.  
  
6.  In the **Debug this application as if it were downloaded from the following URL** text box, enter a URL or network path.  
  
## See Also  
 [How to: Set Custom Permissions for a ClickOnce Application](../Topic/How%20to:%20Set%20Custom%20Permissions%20for%20a%20ClickOnce%20Application.md)   
 [ClickOnce Security](../vs140/Securing-ClickOnce-Applications.md)   
 [Code Access Security for ClickOnce Applications](../Topic/Code%20Access%20Security%20for%20ClickOnce%20Applications.md)   
 [ClickOnce Deployment and Security](../vs140/Securing-ClickOnce-Applications.md)