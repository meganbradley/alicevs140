---
title: "Sample Excel Extension: TechnologyManager Class"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8a7b760d-b5ac-4451-9593-6ac1a0b95cdb
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Sample Excel Extension: TechnologyManager Class
This class extends the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager?qualifyHint=False> class and is responsible for providing core services for the [!INCLUDE[ofprexcel](../vs140/includes/ofprexcel_md.md)] extension. Although the base class has many methods, only a subset of them is used in this sample.  
  
 Some methods just return a property value. Many of the methods are intended to allow the developer to override default algorithms build into the coded UI test engine. These methods throw a <xref:System.NotSupportedException?qualifyHint=False> or return `null`, which tells the framework to use the default algorithm.  
  
 Depending on the complexity of the underlying technology, developing the technology manager code could take from a few weeks to a few months. Excel provides an opportunity to create a potentially very extensive technology manager. This example is intentionally limited to Excel worksheets and cells and uses limited formatting.  
  
 When it is possible, the technology manager code uses the .NET Remoting channel opened by the `Communicator` class to extract information from the Add-In running in the Excel process.  
  
## COM Visibility  
 Notice that this class and each of the element classes that extend the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyElement?qualifyHint=False> class all have the <xref:System.Runtime.InteropServices.ComVisibleAttribute?qualifyHint=False> with a value of `true` to make sure the classes are visible to COM.  
  
## TechnologyName Property  
 This override of the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager.TechnologyName?qualifyHint=True> property must provide a unique and meaningful name that identifies the underlying technology for every other component of the extension. For this extension, the value is "Excel".  
  
## GetControlSupportLevel Method  
 This override of the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager.GetControlSupportLevel?qualifyHint=True> method returns a number that indicates the level of support that the technology manager can offer for the control represented by the provided handle. The higher the returned value, the more the technology manager can support the control. In this case, the method checks the window that contains the control and if it is an Excel Worksheet, the method returns the highest value; otherwise, it returns zero, which indicates that no support is provided.  
  
## Methods to Get an Element  
 There are several important methods that are used by the coded UI testing framework to get an element specific to the technology by providing a handle, a point on the screen, or an element from a different technology. The code for these methods are self-explanatory. The base methods are as follows:  
  
-   <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager.GetFocusedElement?qualifyHint=True>  
  
-   <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager.GetElementFromPoint?qualifyHint=True>  
  
-   <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager.GetElementFromWindowHandle?qualifyHint=True>  
  
-   <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager.GetElementFromNativeElement?qualifyHint=True>  
  
-   <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager.ConvertToThisTechnology?qualifyHint=True>  
  
## ParseQueryId Method  
 When a coded UI test is created, the user can specify property values for some or all the controls in the test. These property values are used by the testing framework to create name-value pairs called search properties that are used to find specific UI controls during the test. All the search properties together represent the value of the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyElement.QueryId?qualifyHint=True> property of every element in the technology, which includes every control. Because a control might have to be found several times during a test, this method gives the technology manager a way to optimize parsing of search properties for the given control. This method also returns a cookie that the framework can use for subsequent searches for that control. This implementation of the method uses the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.AndCondition.Match?qualifyHint=True> method to parse the search properties.  
  
## MatchElement Method  
 To perform a control search by the technology manager, you can implement the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager.Search?qualifyHint=True> method to either return an array of possible matches, or throw the <xref:System.NotSupportedException?qualifyHint=False>, which tells the framework to use its own search algorithm. Either way, you must implement the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager.MatchElement?qualifyHint=False> method where this implementation again uses the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.AndCondition.Match?qualifyHint=True> method.  
  
## Navigation Methods  
 These methods get the parent, children, or siblings of the provided element from the UI hierarchy. The code is simple and clearly commented.  
  
## GetExcelElement Internal Method  
 This internal method takes a window handle and information about an Excel element, and returns the requested Excel element.  
  
## See Also  
 <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager?qualifyHint=False>   
 <xref:System.NotSupportedException?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyElement?qualifyHint=False>   
 <xref:System.Runtime.InteropServices.ComVisibleAttribute?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyElement.QueryId?qualifyHint=False>   
 [Creating a Coded UI Extension to Support Excel](../Topic/Extending%20Coded%20UI%20Tests%20and%20Action%20Recordings%20to%20Support%20Microsoft%20Excel.md)