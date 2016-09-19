---
title: "Find code changes and other history with CodeLens"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f697d7b4-704e-4cac-b13a-bc57d2ff8318
caps.latest.revision: 133
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Find code changes and other history with CodeLens
Stay focused on your work while you find out what happened to your code - without leaving the editor. Find references and changes to your code, linked bugs, work items, code reviews, and unit tests.  
  
> [!NOTE]
>  CodeLens is available only in Visual Studio Enterprise and Visual Studio Professional editions. It is not available in Visual Studio Community edition.  
  
 See where and how the individual parts of your code are used in your solution:  
  
 ![CodeLens indicators in the code editor](../vs140/media/CodeLensOverview.png "CodeLensOverview")  
  
 Contact your team about changes to your code without leaving the editor:  
  
 ![CodeLens &#45; Contact your team](../vs140/media/CodeLensOvervew2.png "CodeLensOvervew2")  
  
 To choose the indicators that you want to see, or to turn CodeLens off and on, go to **Tools**, **Options**, **Text Editor**, **All Languages**, **CodeLens**.  
  
##  <a name="FindReferences"></a> Find references to your code  
 You'll need:  
  
-   Visual Studio Enterprise or Visual Studio Professional  
  
-   Visual C# .NET or Visual Basic .NET code  
  
 Choose the **references** indicator (**Alt + 2**). If you see **0 references**, you have no references from Visual C# or Visual Basic code. This doesn't include references from other items such as XAML and ASPX files.  
  
 ![CodeLens &#45; Choose references indicator](../vs140/media/CodeLensViewReferencesList.png "CodeLensViewReferencesList")  
  
 To view the referencing code, move your mouse on top of the reference.  
  
 ![CodeLens &#45; Peek reference](../vs140/media/CodeLensViewReferencesPeekReference.png "CodeLensViewReferencesPeekReference")  
  
 To open the file containing the reference, double-click the reference.  
  
 To see relationships between this code and its references, [create a code map](../vs140/Map-dependencies-across-your-solutions.md) and choose **Show All References** in the code map shortcut menu.  
  
 ![CodeLens &#45; References on code map](../vs140/media/CodeLensMappedReferences.png "CodeLensMappedReferences")  
  
##  <a name="FindCodeHistory"></a> Find your code's history and linked items  
 Review your code's history to find out what happened to your code. Or, review changes before they're merged into your code so you can better understand how changes in other branches might affect your code.  
  
 You'll need:  
  
-   Visual Studio Enterprise or Visual Studio Professional  
  
-   Team Foundation Server 2013 or later, Visual Studio Team Services, or Git  
  
-   [Lync 2010 or later, or Skype for Business](http://technet.microsoft.com/en-us/lync), to contact your team from the code editor  
  
 For Visual C# .NET or Visual Basic .NET code that's stored with Team Foundation version control (TFVC) or Git, you get CodeLens details at the class and method levels (*code-element-level* indicators). If your Git repository is hosted in TfGit, you also get links to TFS work items.  
  
 ![Code element&#45;level indicators](../vs140/media/CodeLensElementLevelIndicators.png "CodeLensElementLevelIndicators")  
  
 For all other types of files that you can open in the Visual Studio editor, you get CodeLens details for the entire file in one place at the bottom of the window (*file-level* indicators).  
  
 ![File&#45;level CodeLens indicators](../vs140/media/ALMCodeLensFileLevelIndicators.png "ALMCodeLensFileLevelIndicators")  
  
 To use the keyboard to select indicators, press and hold the **ALT** key to display the related number keys.  
  
 ![Press ALT to see the keyboard access numbers](../vs140/media/CodeLensAltKeyIndicators.png "CodeLensAltKeyIndicators")  
  
### Find changes in your code  
 Find who changed your C# or Visual Basic code, and the changes they made, in code-element-level indicators. This is what you see when you use Team Foundation version control (TFVC) in Team Foundation Server or Visual Studio Team Services.  
  
 ![CodeLens: Get change history for your code in TFVC](../vs140/media/CodeLensCodeChanges.png "CodeLensCodeChanges")  
  
 The default time period is the last 12 months. If your code is stored in Team Foundation Server, you can change this by running the [TFSConfig command](assetId:///94424190-3b6b-4f33-a6b6-5807f4225b62) with the [CodeIndex command](../vs140/CodeIndex-Command.md) and the **/indexHistoryPeriod** flag.  
  
 To see a detailed history of all the changes, including those from more than a year ago, choose **Show all file changes**.  
  
 ![Show all code changes](../vs140/media/CodeLensShowsAllChanges.png "CodeLensShowsAllChanges")  
  
 This opens the History window for the changesets.  
  
 ![History window for all code changes](../vs140/media/CodeLensCodeChangesHistory.png "CodeLensCodeChangesHistory")  
  
 When your files are in a Git repository and you choose the code-element-level changes indicator, this is what you see.  
  
 ![CodeLens: Get change history for your code in Git](../vs140/media/CodeLensCodeChangesGit.png "CodeLensCodeChangesGit")  
  
 Find changes for an entire file (except for C# and Visual Basic files) in the file-level indicators at the bottom of the window.  
  
 ![CodeLens: Get code file details](../vs140/media/CodeLensFileLevel.png "CodeLensFileLevel")  
  
 To get more details about a change, right-click that item. Depending on whether you are using TFVC or Git you get a series of options to compare the versions of the file, view details and track the changeset, get the selected version of the file, and email the author of that change. Some of these details appear in Team Explorer.  
  
 You can also see who changed your code over time. This can help you find patterns in your team's changes and assess their impact.  
  
 ![CodeLens: See code changes history as a graph](../vs140/media/CodeLens.png "CodeLens")  
  
#### Find changes in your current branch  
 Suppose your team has multiple branches - a main branch and a child development - to reduce the risk of breaking stable code:  
  
 ![CodeLens: Find when your code was branched](../vs140/media/CodeLensFirstBranchConceptual.png "CodeLensFirstBranchConceptual")  
  
 Find how many people changed your code and how many changes were made (**Alt + 6**) in your main branch:  
  
 ![CodeLens: Find how many changes in your branch](../vs140/media/CodeLensBranchChanges.png "CodeLensBranchChanges")  
  
#### Find when your code was branched  
 Go to your code in the child branch, for example, the Dev branch here. Choose the changes indicator (**Alt + 6**):  
  
 ![CodeLens: Find when your code was branched](../vs140/media/CodeLensFirstBranchScreenshot.png "CodeLensFirstBranchScreenshot")  
  
#### Find incoming changes from other branches  
 ![CodeLens: Find code changes in other branches](../vs140/media/CodeLensBranchChangeCheckinConceptual.png "CodeLensBranchChangeCheckinConceptual")  
  
 …like this bug fix in the Dev branch here:  
  
 ![CodeLens: Change checked into another branch](../vs140/media/CodeLensBranchChangeDevScreenshot.png "CodeLensBranchChangeDevScreenshot")  
  
 You can review this change without leaving your current branch (Main):  
  
 ![CodeLens: See incoming change from another branch](../vs140/media/CodeLensBranchChangeMainScreenshot.png "CodeLensBranchChangeMainScreenshot")  
  
#### Find when changes got merged  
 So you can see which changes are included in your branch:  
  
 ![CodeLens &#45; Merged changes between branches](../vs140/media/CodeLensBranchMergedConceptual.png "CodeLensBranchMergedConceptual")  
  
 For example, your code in the Main branch now has the bug fix from the Dev branch:  
  
 ![CodeLens &#45; Merged chagnes between branches](../vs140/media/CodeLensBranchMergedScreenshot.png "CodeLensBranchMergedScreenshot")  
  
#### Compare an incoming change with your local version (Shift + F10)  
 ![CodeLens: Compare incoming change with local](../vs140/media/CodeLensBranchIncomingChangeMenu.png "CodeLensBranchIncomingChangeMenu")  
  
 You can also double-click the changeset.  
  
#### What do the icons mean?  
  
|**Icon**|**Where did the change come from?**|  
|--------------|-----------------------------------------|  
|![CodeLens: Change from current branch icon](../vs140/media/CodeLensBranchCurrentIcon.png "CodeLensBranchCurrentIcon")|The current branch|  
|![CodeLens &#45; Change from parent branch icon](../vs140/media/CodeLensBranchParentIcon.png "CodeLensBranchParentIcon")|The parent branch|  
|![CodeLens: Change from child branch icon](../vs140/media/CodeLensBranchChildIcon.png "CodeLensBranchChildIcon")|A child branch|  
|![CodeLens &#45; Change from peer branch icon](../vs140/media/CodeLensBranchPeerIcon.png "CodeLensBranchPeerIcon")|A peer branch|  
|![CodeLens &#45; Change from branch further away icon](../vs140/media/CodeLensBranchFurtherAwayIcon.png "CodeLensBranchFurtherAwayIcon")|A branch further away than a parent, child, or peer|  
|![CodeLens: Merge from parent icon](../vs140/media/CodeLensBranchMergeFromParentIcon.png "CodeLensBranchMergeFromParentIcon")|A merge from the parent branch to a child branch|  
|![CodeLens: Merge from child branch icon](../vs140/media/CodeLensBranchMergeFromChildIcon.png "CodeLensBranchMergeFromChildIcon")|A merge from a child branch to the parent branch|  
|![CodeLens: Merge from unrelated branch icon](../vs140/media/CodeLensBranchMergeFromUnrelatedIcon.png "CodeLensBranchMergeFromUnrelatedIcon")|A merge from an unrelated branch (baseless merge)|  
  
### Find linked work items  
 ![CodeLens &#45; Find work items for specific code](../vs140/media/CodeLensWorkItems.png "CodeLensWorkItems")  
  
### Find linked code reviews  
 ![CodeLens &#45; View code review requests](../vs140/media/CodeLensCodeReviews.png "CodeLensCodeReviews")  
  
### Find linked bugs  
 ![CodeLens &#45; Find bugs linked to changesets](../vs140/media/CodeLensBugsChangesets.png "CodeLensBugsChangesets")  
  
### Contact the owner of an item  
 ![Contact the owner of an item](../vs140/media/CodeLensContactItemOwner.png "CodeLensContactItemOwner")  
  
 Open the shortcut menu for an item to see the contact options. If you have Lync or Skype for Business installed, you see these options:  
  
 ![Contact options for an item](../vs140/media/CodeLensItemContactMenu.png "CodeLensItemContactMenu")  
  
##  <a name="FindRunUnitTests"></a> Find unit tests for your code  
 Find out more about unit tests that exist for your code without opening Test Explorer. You'll need:  
  
-   Visual Studio Enterprise or Visual Studio Professional  
  
-   Visual C# .NET or Visual Basic .NET code  
  
-   A [unit test project](../Topic/Unit%20Test%20Your%20Code.md) that has unit tests for your application code  
  
1.  Go to application code that has unit tests.  
  
2.  Review the tests for that code (**Alt + 3**).  
  
     ![CodeLens &#45; Choose test status in code editor](../vs140/media/CodeLensChooseTestIndicator.png "CodeLensChooseTestIndicator")  
  
3.  If you see a warning icon ![CodeLens &#45; Unit tests not yet run warning](../vs140/media/CodeLensTestWarningIcon.png "CodeLensTestWarningIcon"), run the tests.  
  
     ![CodeLens &#45; View unit tests not run yet](../vs140/media/CodeLensTestsNotYetRun.png "CodeLensTestsNotYetRun")  
  
4.  To review a test's definition, double-click the test item in the CodeLens indicator window to open the code file in the editor.  
  
     ![CodeLens &#45; Go to unit test definition](../vs140/media/CodeLensUnitTestDefinition.png "CodeLensUnitTestDefinition")  
  
5.  Review the test’s results. Choose the test status indicator (![CodeLens &#45; Unit test failed icon](../vs140/media/CodeLensTestFailedIcon.png "CodeLensTestFailedIcon") or ![CodeLens &#45; Unit test passed icon](../vs140/media/CodeLensTestPassedIcon.png "CodeLensTestPassedIcon")), or press **Alt + 1**.  
  
     ![CodeLens &#45; See unit test result](../vs140/media/CodeLensUnitTestResult.png "CodeLensUnitTestResult")  
  
6.  To see how many people changed this test, who changed this test, or how many changes were made to this test, [find the code's history](#FindCodeHistory).  
  
##  <a name="QA"></a> Q & A  
  
###  <a name="ChangeOrTurnOff"></a> Q: How do I turn CodeLens off or on? Or choose which indicators to see?  
 **A:**  You can turn indicators off or on, except for the references indicator. Go to **Tools**, **Options**, **Text Editor**, **All Languages**, **CodeLens**.  
  
 When the indicators are turned on, you can also open the CodeLens options from the indicators.  
  
 ![CodeLens &#45; Turn indicators off or on](../vs140/media/CodeLensTurnOffOnIndicatorsFromCode.png "CodeLensTurnOffOnIndicatorsFromCode")  
  
 Turn CodeLens file-level indicators on and off using the chevron icons at the bottom of the editor window.  
  
 ![Turn file&#45;level indicators on and off](../vs140/media/CodeLensFileLevelOnAndOff.png "CodeLensFileLevelOnAndOff")  
  
###  <a name="NoIndicators"></a> Q: Where is CodeLens?  
 **A:** CodeLens appears in Visual C# .NET and Visual Basic .NET code at the method, class, indexer, and property level. CodeLens appears at the file level for all other types of files.  
  
-   Make sure CodeLens is turned on. Go to **Tools**, **Options**, **Text Editor**, **All Languages**, **CodeLens**.  
  
-   If your code is stored in TFS, make sure that code indexing is turned on by using the [CodeIndex command](../vs140/CodeIndex-Command.md) with the [TFS Config command](assetId:///94424190-3b6b-4f33-a6b6-5807f4225b62).  
  
-   TFS-related indicators appear only when work items are linked to the code and when you have permissions to open linked work items. [Confirm that you have team member permissions.](assetId:///f58805de-ba61-4d09-8f2d-d3ab9662ecfd)  
  
-   Unit test indicators don't appear when application code doesn't have unit tests. Test status indicators appear automatically in test projects. If you know that your application code has unit tests, but the test indicators don't appear, try building the solution (**Ctrl + Shift + B**).  
  
### Q: Why don't I see the work item details for a commit?  
 **A:** This might happen because CodeLens can't find the work items in TFS. Check that you're connected to the team project that has those work items and that you have permissions to see those work items. This might also happen if the commit description has incorrect information about the work item IDs in TFS.  
  
###  <a name="NoLync"></a> Q: Why don't I see the Lync or Skype indicators?  
 **A:** They don't appear if you're not signed into Lync or Skype for Business, don't have one of these installed, or don't have a supported configuration. But you can still send mail:  
  
 ![CodeLens &#45; Contact changeset owner by mail](../vs140/media/CodeLensCodeSendMailChangesetNoLync1.png "CodeLensCodeSendMailChangesetNoLync1")  
  
 **Which Lync and Skype configurations are supported?**  
  
-   Skype for Business (32-bit or 64-bit)  
  
-   Lync 2010 or later alone (32-bit or 64-bit), but not Lync Basic 2013 with Windows 8.1  
  
 CodeLens doesn't support having different versions of Lync or Skype installed. They might not be localized for all localized versions of Visual Studio.  
  
### Q: How do I change the font and color for CodeLens?  
 **A:** Go to **Tools**, **Options**, **Environment**, **Fonts and Colors**.  
  
 ![CodeLens &#45; Change font and color settings](../vs140/media/CodeLensOptionsFontsColorsSettings.png "CodeLensOptionsFontsColorsSettings")  
  
 To use the keyboard:  
  
1.  Press **Alt + T + O** to open the **Options** box.  
  
2.  Press **Up Arrow** or **Down Arrow** to go to the **Environment** node, then press **Left Arrow** to expand the node.  
  
3.  Press **Down Arrow** to go to **Fonts and Colors**.  
  
4.  Press **TAB** to go to the **Show settings for** list, and then press **Down Arrow** to select **CodeLens**.  
  
### Q: Can I move the CodeLens heads-up display?  
 **A:** Yes, choose ![CodeLens &#45; Dock as a window](../vs140/media/CodeLensDockWindow.png "CodeLensDockWindow") to dock CodeLens as a window.  
  
 ![Dock the CodeLens indicator window](../vs140/media/CodeLensSelectDockWindow.png "CodeLensSelectDockWindow")  
  
 ![The docked CodeLens References window](../vs140/media/CodeLensReferencesDockedWindow.png "CodeLensReferencesDockedWindow")  
  
### Q: How do I refresh the indicators?  
 **A:** This depends on the indicator:  
  
-   **References**: This indicator updates automatically when the code changes. If you have this indicator docked as a separate window, refresh the indicator manually here:  
  
     ![CodeLens &#45; Dock as window](../vs140/media/CodeLensViewReferencesDocked.png "CodeLensViewReferencesDocked")  
  
-   **Team**: Refresh these indicators manually here:  
  
     ![CodeLens &#45; Refresh indicators](../vs140/media/CodeLensRefreshIndicatorsFromCode.png "CodeLensRefreshIndicatorsFromCode")  
  
-   **Test**: [Run all the tests or specific tests](#FindRunUnitTests) to refresh this indicator.  
  
###  <a name="LocalVersion"></a> Q: What's "Local Version"?  
 **A:** The **Local Version** arrow points at the most recent changeset in your local version of this file. When the server has more recent changesets, they appear above or below the **Local Version** arrow, depending on the order used to sort the changesets.  
  
### Q: Can I manage how CodeLens processes code to show history and linked items?  
 **A:** Yes, if your code is in TFS, use the [CodeIndex command](../vs140/CodeIndex-Command.md) with the [TFS Config command](assetId:///94424190-3b6b-4f33-a6b6-5807f4225b62).