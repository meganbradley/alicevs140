---
title: "Walkthrough: Adding Custom XAML to the Start Page"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9af4d5f9-1cfc-4221-aea7-c8cd3f7571a6
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Walkthrough: Adding Custom XAML to the Start Page
This walkthrough shows how to create a custom Visual Studio Start Page that contains a Web browser.  
  
## Adding Custom XAML  
  
1.  Create a Start Page by following the instructions in [Creating a Custom Start Page](../Topic/Creating%20a%20Custom%20Start%20Page.md).  
  
2.  In the MainWindow.xaml file, find the <Grid\> section.  
  
3.  Add a <TabControl\> element and a <TabItem\> inside the < Grid> element, as shown in the following example.  
  
    ```xml  
    <Grid>  
        <TabControl>  
            <TabItem Header="Bing" Height="Auto">  
                <Frame Source="http://www.bing.com" />  
            </TabItem>  
        </TabControl>  
    </Grid>  
    ```  
  
4.  Add a second <TabItem\>, with a <Button\> element that opens a new project:  
  
    ```xml  
    <Grid>  
        <TabControl>  
            <TabItem Header="MyButton" Height="Auto">  
                <Button Name="btnNewProj" Content="New Project"   
                    Command="{x:Static vscom:VSCommands.ExecuteCommand}"  
                    CommandParameter="File.NewProject" >  
                </Button>  
            </TabItem>  
            <TabItem Header="Bing" Height="Auto">  
                <Frame Source="http://www.bing.com" />  
            </TabItem>  
        </TabControl>  
    </Grid>  
    ```  
  
## Testing the Custom Start Page  
  
1.  Press F5.  
  
     The experimental instance of Visual Studio opens, with the custom Start Page installed but not selected.  
  
2.  In the experimental instance of Visual Studio, open the **Tools /Options / Environment** page.  
  
3.  Select **Startup**. On the **Customize Start Page** list, select your .xaml file, and click **OK**.  
  
4.  On the **View** menu, click **Start Page**.  
  
5.  Click the **Bing** tab.  
  
     You should see a Bing web page.  
  
6.  Click the **MyButton** tab.  
  
     You should see a **MyProject** button, which opens the **New Project** dialog.  
  
7.  Close the experimental instance.  
  
## Applying the Custom Start Page  
  
#### To test the custom Start Page  
  
1.  In **Tools / Options / Environment**, select **Startup**. On the **Customize Start Page** list, select your .xaml file, and click **OK**.  
  
## Next Steps  
 The Visual Studio Start Page now contains a tab that displays a Web browser tab and a MyButton tab. You can create custom Start Pages that have other functionality by using the *code-behind* model to add a custom .dll, as shown in [Walkthrough: Adding a DLL Reference to the Start Page](../Topic/Adding%20User%20Control%20to%20the%20Start%20Page.md). You can share custom Start Pages with other users by publishing the resulting .vsix file to the [Visual Studio Gallery](http://go.microsoft.com/fwlink/?LinkID=123847) Web site, or to another Web site or network share. For more information, see [Deploying Custom Start Pages](../vs140/Deploying-Custom-Start-Pages.md).  
  
## See Also  
 [Customizing the Start Page](../vs140/Customizing-the-Start-Page-for-Visual-Studio.md)   
 [WPF Container Controls](assetId:///a0177167-d7db-4205-9607-8ae316952566)