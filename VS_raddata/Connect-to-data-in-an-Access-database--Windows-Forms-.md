---
title: "Connect to data in an Access database (Windows Forms)"
ms.custom: na
ms.date: 10/07/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - aspx
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4159e815-d430-4ad0-a234-e4125fcbef18
caps.latest.revision: 29
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# Connect to data in an Access database (Windows Forms)
You can connect to an Access database (either an .mdf file or an .accdb file) by using Visual Studio. After you define the connection, the data appears in the **Data Sources** window. From there, you can drag tables or views onto your forms. If you want to understand how the project system in Visual Studio manages these local database files, see [How to: Manage Local Data Files in Your Project](../VS_raddata/How-to--Manage-Local-Data-Files-in-Your-Project.md).  
  
## Prerequisites  
 To use these procedures, you need a Windows Forms application project, and either an Access database (.accdb file) or an Access 2000–2003 database (.mdb file). Follow the procedure that corresponds to your file type.  
  
## Creating the dataset for an .accdb file  
 You can connect to databases created through Access 2013, Office 365, Access 2010, or Access 2007 by using the following procedure.  
  
#### To create the dataset  
  
1.  Open the Windows Forms application to which you want to connect data.  
  
2.  On the **View** menu, select **Other Windows** > **Data Sources**.  
  
     ![View Other Windows Data Sources](../VS_raddata/media/ViewDataSources.png "ViewDataSources")  
  
3.  In the **Data Sources** window, click **Add New Data Source**.  
  
     ![Add New Data Source](../VS_raddata/media/dataAddNewDataSource.png "dataAddNewDataSource")  
  
4.  Select **Database** on the **Choose a Data Source Type** page, and then select **Next**.  
  
5.  Select **Dataset** on the **Choose a Database Model** page, and then select **Next**.  
  
6.  On the **Choose your Data Connection** page, select **New Connection** to configure a new data connection.  
  
7.  Change the **Data source** to **.NET Framework Data Provider for OLE DB**.  
  
     ![Change Data Provider to OLE DB](../VS_raddata/media/dataChangeDataSourceOLEDB.png "dataChangeDataSourceOLEDB")  
  
    > [!IMPORTANT]
    >  Although a data source of **Microsoft Access Database File (OLE DB)** might seem like the right choice, you use that data-source type only for .mdb database files.  
  
8.  In **OLE DB Provider**, select **Microsoft Office 12.0 Access Database Engine OLE DB Provider**.  
  
     ![OLE DB Provider Microsoft Office 12.0 Access](../VS_raddata/media/dataOLEDBProviderOffice12Access.png "dataOLEDBProviderOffice12Access")  
  
9. In **Server or file name**, specify the path and name of the .accdb file to which you want to connect, and then select **OK**.  
  
    > [!NOTE]
    >  If the database file has a user name and password, specify them before you select **OK**.  
  
10. Select **Next** on the **Choose your Data Connection** page.  
  
11. Select **Next** on the **Save connection string to the Application Configuration file** page.  
  
12. Expand the **Tables** node on the **Choose your Database Objects** page.  
  
13. Select whatever tables or views you want in your dataset, and then select **Finish**.  
  
     The dataset is added to your project, and the tables and views appear in the **Data Sources** window.  
  
## Creating the dataset for an .mdb file  
 You create the dataset by running the **Data Source Configuration Wizard**.  
  
#### To create the dataset  
  
1.  Open the Windows Forms application to which you want to connect data.  
  
2.  On the **View** menu, select **Other Windows** > **Data Sources**.  
  
     ![View Other Windows Data Sources](../VS_raddata/media/ViewDataSources.png "ViewDataSources")  
  
3.  In the **Data Sources** window, click **Add New Data Source**.  
  
4.  Select **Database** on the **Choose a Data Source Type** page, and then select **Next**.  
  
5.  Select **Dataset** on the **Choose a Database Model** page, and then select **Next**.  
  
6.  On the **Choose your Data Connection** page, select **New Connection** to configure a new data connection.  
  
7.  If the data source is not **Microsoft Access Database File (OLE DB)**, select **Change** to open the **Change Data Source** dialog box and select **Microsoft Access Database File**, and then select **OK**.  
  
8.  In the **Database file name**, specify the path and name of the .mdb file to which you want to connect, and then select **OK**.  
  
     ![Add Connection Access Database File](../VS_raddata/media/dataAddConnectionAccessMDB.png "dataAddConnectionAccessMDB")  
  
9. Select **Next** on the **Choose your Data Connection** page.  
  
10. Select **Next** on the **Save connection string to the Application Configuration file** page.  
  
11. Expand the **Tables** node on the **Choose your Database Objects** page.  
  
12. Select whatever tables or views you want in your dataset, and then select **Finish**.  
  
     The dataset is added to your project, and the tables and views appear in the **Data Sources** window.  
  
## Security  
 Storing sensitive information (such as a password) can affect the security of your application. Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database. For more information, see [Protecting Connection Information](../Topic/Protecting%20Connection%20Information.md).  
  
## Next Steps  
 The dataset that you just created is now available in the **Data Sources** window. You can now perform any of the following tasks:  
  
-   Select items in the **Data Sources** window and drag them onto your form (see [Bind Windows Forms controls to data in Visual Studio](../VS_raddata/Bind-Windows-Forms-controls-to-data-in-Visual-Studio.md)).  
  
-   Open the data source in the [Dataset Designer](../VS_raddata/Creating-and-Editing-Typed-Datasets.md) to add or edit the objects that make up the dataset.  
  
-   Add validation logic to the <xref:System.Data.DataTable.ColumnChanging?qualifyHint=False> or <xref:System.Data.DataTable.RowChanging?qualifyHint=False> event of the data tables in the dataset (see [Validate data in datasets](../VS_raddata/Validate-data-in-datasets.md)).  
  
## See Also  
 [Connecting to Data in Visual Studio](../VS_raddata/Connecting-to-Data-in-Visual-Studio.md)   
 [Preparing Your Application to Receive Data](../Topic/Preparing%20Your%20Application%20to%20Receive%20Data.md)   
 [Fetching Data into Your Application](../VS_raddata/Fetching-Data-into-Your-Application.md)   
 [Bind controls to data in Visual Studio](../VS_raddata/Bind-controls-to-data-in-Visual-Studio.md)   
 [Editing Data in Your Application](../VS_raddata/Editing-Data-in-Your-Application.md)   
 [Validating Data](../Topic/Validating%20Data.md)   
 [Saving Data](../VS_raddata/Saving-Data.md)   
 [Data Walkthroughs](../Topic/Data%20Walkthroughs.md)