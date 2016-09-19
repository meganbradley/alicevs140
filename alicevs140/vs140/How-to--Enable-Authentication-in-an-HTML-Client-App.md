---
title: "How to: Enable Authentication in an HTML Client App"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - lightswitch
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d600485c-6c2d-4e5e-a9c8-1d1aa31754b3
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Enable Authentication in an HTML Client App
In LightSwitch, you can make your HTML client app more secure by preventing unauthorized users from reading, changing, or deleting data. If you implement authentication, users must prove their identities before they can access the application.  
  
> [!NOTE]
>  The process for setting permissions differs for Silverlight clients – see [How to: Enable Authentication in an Silverlight Client App](../vs140/How-to--Enable-Authentication-in-a-Silverlight-Client-App.md). LightSwitch apps that have been enabled for SharePoint use SharePoint authentication for access control.  
  
 If you have many users, you can also manage access more easily by creating user roles that have various levels of access to particular screens and data and then assigning each user to the appropriate role. For example, a payroll application could allow employees to view, but not change, their payroll information. However, a payroll supervisor could be given permission to view and change the employee information. The employees would be assigned to the Employee role and the supervisor would be assigned to the Supervisor role.  
  
 You can also administer permissions more easily by adding users to security groups in Active Directory and then assigning permissions to those groups. Because membership and permissions are inherited, you can grant and deny permissions for not only a group but also all of its subgroups by making a single change. For example, you can add *Bob* to the *Sales* group in Active Directory. If *Sales* is a subgroup of *Marketing*, any permission that you grant to *Marketing* would also be granted to *Bob*.  
  
 Authentication and authorization can be implemented on the server by writing Visual Basic or C# code; to implement it at the screen level you’ll need to add queries on the server and base your HTML screens on those queries, then write JavaScript code to enable or disable screens based on permissions. You’ll also need to add a Silverlight client in order to administer users and roles. Silverlight-based **Users** and **Roles** screens will be available to the person designated as the **Application Administrator** during publishing.  
  
-   [Authentication](../vs140/How-to--Enable-Authentication-in-an-HTML-Client-App.md#auth)  
  
-   [Permissions](../vs140/How-to--Enable-Authentication-in-an-HTML-Client-App.md#perm)  
  
-   [Securing the Server](../vs140/How-to--Enable-Authentication-in-an-HTML-Client-App.md#server)  
  
-   [Securing the Client](../vs140/How-to--Enable-Authentication-in-an-HTML-Client-App.md#client)  
  
-   [Administration](../vs140/How-to--Enable-Authentication-in-an-HTML-Client-App.md#admin)  
  
##  <a name="auth"></a> Authentication  
 The first step in securing your application is to enable authentication. You can use either Forms authentication or Windows authentication. Forms authentication is managed by the application itself, and a user must supply a username and a password to access the application. In Windows authentication, the credentials that were used to log on to the computer where the application is run are used to authenticate the application user, and no additional username or password is required. In both cases, an application administrator maintains a list of authorized users; in Forms authentication, the administrator also maintains encrypted passwords.  
  
#### To enable authentication  
  
1.  In **Solution Explorer**, open the shortcut menu for the **Properties** node, and then choose **Open**.  
  
2.  In the **Application Designer**, choose the **Access Control** tab.  
  
3.  In the **Select the type of authentication to use:** list, choose either **Use Windows authentication** or **Use Forms authentication**.  
  
     If you chose **Use Windows authentication**, choose either the **Allow only users specified in the Users screen of your application** option button or the **Allow any authenticated Windows user** option button.  
  
     The application will now require users to provide credentials in order to access the application.  
  
##  <a name="perm"></a> Permissions  
 The next step in securing your HTML client application is to create permissions. First, define a permission object in the **Application Designer**. Then, you can reference the object in code, in one of the `Can` methods such as *<Entity\>*`CanUpdate`. Code in these methods typically checks whether the current user or role has the permission, and then allows the operation only if permission is validated.  
  
 To test your code, run the application as both a user who has the permission and as a user who does not.  By setting debug permissions, you can impersonate a user when you test or debug the application.  
  
#### To create a permission  
  
1.  In **Solution Explorer**, open the shortcut menu for the **Properties** node, and then choose **Open**.  
  
2.  In the **Application Designer**, choose the **Access Control** tab.  
  
3.  In the **Define permissions or select permissions to use for debugging** grid, in the **Name** column, choose **<Add New Permission\>**, and then enter a programmatic name for the permission.  
  
     The name must begin with an alphabetical character, and it can only contain alphabetical or numeric characters, or underscores.  
  
4.  In the **Display Name** column, enter the name of the permission as you want it to appear in the screen that the application administrator will use to assign roles.  
  
5.  In the **Description** column, enter a description of the permission.  
  
#### To enable permissions for debugging  
  
1.  In **Solution Explorer**, open the shortcut menu for the **Properties** node, and then choose **Open**.  
  
2.  In the **Application Designer**, choose the **Access Control** tab.  
  
3.  In the **Define permissions or select permissions to use for debugging** grid, choose the permission that you want to enable for debugging, and then select the **Granted for debug** check box.  
  
##  <a name="server"></a> Securing the Server  
 The next step is to add code that checks for permissions on the server tier using access control methods. You can write code in an entity method such as `CanUpdate` or in a query method such as `CanExecute`. As a best practice, you should always secure server tier using access control methods in order to protect the data in your system.  
  
#### To write code to set permissions for an entity  
  
1.  In **Solution Explorer**, open the shortcut menu for an entity node, and then choose **Open**.  
  
     The Entity Designer for that entity opens.  
  
2.  In the Entity Designer, on the **Perspective** bar, choose **Server**.  
  
3.  Expand the **Write Code** list and choose a *EntityName*`_Can`*Operation* method, where *EntityName* is the name of the entity, and *Operation* is the name of the operation for which you want to write code.  
  
    > [!NOTE]
    >  The available methods vary by context. Some examples are `CanInsert`, `CanDelete` and `CanUpdate`.  
  
4.  In the **Code Editor**, enter the code that you want in the *EntityName*`_Can`*Operation* method.  
  
     For example, code to allow a user to update a *Products* entity based on a permission named *Can_Edit_Products* would look like this:  
  
    ```vb  
    Private Sub Products_CanUpdate(ByRef result As Boolean)  
                If Application.User.HasPermission(Can_Edit_Products) Then  
                    result = True  
                Else  
                    result = False  
                End If  
  
            End Sub  
    ```  
  
    ```c#  
    private void Products_CanUpdate(ref bool result)  
    {  
    if (Application.User.HasPermission(Can_Edit_Products)) {  
    result = true;  
    } else {  
    result = false;  
    }  
  
    }  
    ```  
  
#### To write code to set permissions for a query  
  
1.  In **Solution Explorer**, open the shortcut menu for a query node, and then choose **Open**.  
  
     The **Query Designer** for that query opens.  
  
2.  In the **Write Code** list, choose the *QueryName*`_CanExecute` method, where *QueryName* is the name of the query.  
  
3.  In the **Code Editor**, enter the code that you want in the *QueryName*`_CanExecute` method.  
  
     For example, code to allow a user to execute a *ViewProducts* query based on a permission named *Can_View_Products* would look like this:  
  
    ```vb  
    Private Sub ViewProducts_CanExecute(ByRef result As Boolean)  
                If Application.User.HasPermission(Can_View_Products) Then  
                    result = True  
                Else  
                    result = False  
                End If  
  
            End Sub  
    ```  
  
    ```c#  
    private void ViewProducts_CanExecute(ref bool result)  
    {  
    if (Application.User.HasPermission(Can_View_Products)) {  
    result = true;  
    } else {  
    result = false;  
    }  
  
    }  
    ```  
  
##  <a name="client"></a> Securing the Client  
 A common scenario is to restrict access to a screen to only authorized users. For example, all users might be able to view pricing information, but only users in the Accounting department are able to change it. To do this in an HTML client screen, you must first create a query that checks for permission in the `CanExecute` method, and then write JavaScript code in the `created` method of the screen to enable or disable UI elements.  
  
> [!NOTE]
>  For an example of code to check for permission, see "To write code to set permissions for a query" earlier in this topic.  
  
#### To add a query to a screen  
  
1.  In the screen designer, on the toolbar, choose the **Add Data Item** button.  
  
2.  In the **Add Data Item** dialog box, choose the **Query** option button, and then choose your query in the list.  
  
3.  In the content tree, choose the UI element that you want to enable or disable. This is typically the button that launches the screen to which you want to restrict access.  
  
4.  In the **Properties** window, make note of the **Name** property for the UI element. You’ll need this in order to write the code.  
  
#### To write code to set permissions for a screen  
  
1.  In the screen designer, choose the Screen node, and then on the toolbar expand the **Write Code** list and choose **created**.  
  
2.  In the **Code Editor**, enter the code in the *ScreenName*`_created` method.  
  
     For example, code to enable or disable a button named *Edit* based on a query named *EditProducts* would look like this:  
  
    ```javascript  
    myapp.ViewProducts.created = function (screen) {  
        screen.getEditProducts().then (function success() {  
            screen.findContentItem("Edit").isEnabled = true;  
        }, function error() {  
            screen.findContentItem("Edit").isEnabled = false;  
        })  
    };  
    ```  
  
     The code calls the query on the screen and it will fail if the user doesn’t have permission to execute it, invoking the error handler. The button is enabled only if the user’s permission is verified. To hide the button rather than disabling it, use `isVisible` instead of **isEnabled**.  
  
    > [!NOTE]
    >  This method will also disable the button if the query fails for some other reason. For a more robust solution that requires more complicated code, see the blog post [Using LightSwitch ServerApplicationContext and WebAPI to Get User Permissions](http://blogs.msdn.com/b/bethmassi/archive/2013/04/17/using-lightswitch-serverapplicationcontext-and-webapi-to-get-user-permissions.aspx).  
  
##  <a name="admin"></a> Administration  
 The final step in enabling authentication is to add the screens needed to administer the application. In an HTML client application, you must add a Silverlight client to the solution. This provides the default **Users** and **Roles** screens needed for administration. The Silverlight client application and screens are only visible to the person designated as the default administrator during publishing, or to any users that are subsequently granted **Administrative** permissions.  
  
#### To add administration screens  
  
1.  In **Solution Explorer**, open the shortcut menu for the top-level application node and choose **Add Client**.  
  
2.  In the **Add Client** dialog box, choose the **Desktop Client** icon.  
  
3.  In the **Client Name** text box, enter a name for the client, for example *Administration*, and then choose the **OK** button.  
  
#### To define an administrator  
  
-   Follow the steps in [Administering a LightSwitch Application](../vs140/Administering-a-LightSwitch-Application.md).  
  
    > [!IMPORTANT]
    >  If authentication is enabled and you haven’t defined a default administrator, you won’t be able to access the published application.  
  
## See Also  
 [HTML Client Screens for LightSwitch Apps](../vs140/HTML-Client-Screens-for-LightSwitch-Apps.md)   
 [Administering a LightSwitch Application](../vs140/Administering-a-LightSwitch-Application.md)   
 [How to: Enable Authentication in an Silverlight Client App](../vs140/How-to--Enable-Authentication-in-a-Silverlight-Client-App.md)   
 [Using LightSwitch ServerApplicationContext and WebAPI to Get User Permissions](http://blogs.msdn.com/b/bethmassi/archive/2013/04/17/using-lightswitch-serverapplicationcontext-and-webapi-to-get-user-permissions.aspx)