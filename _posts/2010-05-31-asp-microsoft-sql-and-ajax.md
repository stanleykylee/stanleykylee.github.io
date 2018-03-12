---
title: ASP, Microsoft SQL and AJAX
date: 2010-05-31 22:09:41.000000000 -07:00
category: blog
tag:
- work
- AJAX
- ASP
- programming
- SQL Server
---
<p>Well I haven't done web programming for awhile now and getting back into it was a slow start but I was able to get through it. I'll have to admit, at first Google was my best friend. However, soon I found that the <a href="http://msdn.microsoft.com/en-us/library/8bhzsw6t(v=VS.100).aspx" target="_blank">MSDN documentation</a> is actually not too bad if you understand the programming syntax and wording (meaning you're not a total novice at programming).</p>
<p>Many articles can be found online that tell you how to make your first ASP page and connect it to MS SQL, so I'll just summarize the bits that took me the most time<strong>:</strong></p>
<p><strong>1. Web.config</strong>:<br />
This is a file that is used to house various configurations. I used it to turn off the customErrors so that I could do debugging. The other item I configured here was the connectionStrings - used to create a connection to the database.</p>
```
<configuration>
<system.web>
<customerrors mode="Off" />
</system.web>
<connectionstrings>
<add name="connName" connectionstring="Data Source=.\SQLEXPRESS;Initial Catalog=dbName;Persist Security Info=True;User ID=sa;Password=password" providername="System.Data.SqlClient" />
</connectionstrings>
</configuration>
```
<p><strong>2. asp:SqlDataSource</strong>:</p>
<p>This is the container used to define your SQL Query. The main item to note with this is the ConnectionString and ProviderName settings. Because we have defined these within the Web.config file, we merely direct the container to retrieve the values from the Web.config file.</p>
```
<asp:sqldatasource id="generatedDataSource" runat="server" connectionstring="<%$ ConnectionStrings:connName %>" providername="<%$ ConnectionStrings:connName.ProviderName %>" />
```
<p><strong>3. asp:Panel and asp:DataList</strong>:<br />
These two items are the containers for the items that are returned from your SQL Query. I have used the Panel to enclose the DataList in order to enable scrollbars. By default DataList only supports a limited list of formatting options. These can be found in the MSDN documentation as well. However in order to show scrollbars in a pre-defined area a Panel must be used.</p>
```
<asp:panel runat="server" bordercolor="Black" style="width: 650px; height: 400px; overflow: auto">
<asp:datalist id="generatedDataList" datasourceid="generatedDataSource" onload="CheckClicked" runat="server" repeatcolumns="3">
<itemtemplate><%# Eval("tableCol1") %></itemtemplate>
</asp:datalist>
</asp:panel>
```
<p><strong>4. Script generated SQL Query</strong>:<br />
The final item that fell in place for my particular project was the script generated SQL Query. I was able to generate the Query from multiple results returned by multiple CheckBoxLists, however in order to re-display the resulting script generated SQL Query I had to set it to the DataList. To do this, assign the sqlDataSource a SelectCommand value.</p>
```
generatedDataSource.SelectCommand = SQLQuery;
```
<p>Have fun!</p>
