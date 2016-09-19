---
title: "How to: Configure Noise Reduction in Report Views"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b07e0375-bb73-47e3-8d1d-b9b492fb16c9
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Configure Noise Reduction in Report Views
Performance reports can be configured for noise reduction by limiting the amount of data that is presented in the Call Tree view and the Allocation view. By using noise reduction, performance problems are more prominent. This is useful when you analyze performance reports.  
  
 Noise reduction configuration options include the following settings:  
  
-   **Trimming** When a report is analyzed, the view will omit functions that fall in the value and threshold settings that you have configured, as described in the trimming procedure that follows. By default, trimming is enabled.  
  
-   **Folding** If you enable folding, consecutive functions on a path that meet the settings that you have configured will be merged, as described in the folding procedure that follows. By default, folding is enabled by default.  
  
### To configure trimming for a performance report  
  
1.  When either a Call Tree view or Allocation view is displayed in the generated report, on the **Developer** menu, click **Profiler** and then click **Noise Reduction Options**.  
  
     The **Noise Reduction** dialog box appears.  
  
2.  To enable trimming, follow these steps:  
  
    1.  Select **Enable Trimming**. This is the default setting.  
  
        > [!NOTE]
        >  If noise reduction is enabled, an information bar will display in the report. For more information, see [Call Tree View](../vs140/Call-Tree-View.md) and [Allocation View](../vs140/.NET-Memory-Allocations-View.md).  
  
    2.  Configure the value setting by using the **Value** drop-down list and choosing the applicable setting.  
  
    3.  Configure the desired threshold setting by typing a percentage value in the **Threshold** text box.  
  
    4.  To enable the noise reduction warning in the generated report, select **Display warning when Noise Reduction is enabled**. This is the default setting.  
  
3.  To disable trimming, clear **Enable Trimming**.  
  
4.  Click **OK**.  
  
### To configure folding for a performance report  
  
1.  On the **Developer** menu, click **Profiler** and then click **Noise Reduction Options**.  
  
     The **Noise Reduction** dialog box appears.  
  
2.  To enable folding, follow these steps:  
  
    1.  Select **Enable Folding**. This is the default setting.  
  
        > [!NOTE]
        >  If noise reduction is enabled, an information bar will display in the report. For more information, see [Call Tree View](../vs140/Call-Tree-View.md) and [Allocation View](../vs140/.NET-Memory-Allocations-View.md).  
  
    2.  Configure the value setting by using the **Value** drop-down list and selecting the applicable setting.  
  
    3.  Configure the desired threshold setting by typing a percentage value in the **Threshold** text box.  
  
    4.  To enable the noise reduction warning in the generated report, select **Display warning when Noise Reduction is enabled**. This is the default setting.  
  
3.  To disable folding, clear **Enable Folding**.  
  
4.  Click **OK**.  
  
## See Also  
 [Customizing Report Views](../vs140/Customizing-Performance-Tools-Report-Views.md)   
 [How to: Exclude or Include Short Functions from Instrumentation](../vs140/How-to--Exclude-or-Include-Short-Functions-from-Instrumentation.md)   
 [Call Tree View](../vs140/Call-Tree-View.md)   
 [Allocation View](../vs140/.NET-Memory-Allocations-View.md)