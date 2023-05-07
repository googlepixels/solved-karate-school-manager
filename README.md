Download Link: https://assignmentchef.com/product/solved-karate-school-manager
<br>
<p class="ui header product-top-header" title="Karate School Manager Solution"><strong>iLab Overview</strong><strong>Scenario/Summary</strong>Suppose you are a black belt in the Kyoshi Karate School and you would like to create a management application with the following capabilities:1. display a list of all members;2. permit the user to sort on any column, edit individual rows, and delete rows;3. add new entries to the members table; and4. find a member by letting the user enter a partial last name.

<strong>Deliverables</strong>NOTESubmit your assignment to the Dropbox, located at the top of this page. For instructions on how to use the Dropbox, read these step-by-step instructions.(See the Syllabus section “Due Dates for Assignments &amp; Exams” for due dates.)You will create a searchable member database application. A ComboBox control will present a list of first and last names. When the user selects a name, a DataGridView control will fill with member information.Grading RubricThe criteria used for grading your iLab are as follows.TaskPointsCreate New Application and Set Main Form Properties 5 pointsAdd All User Controls 5 pointsTest File (Screenshot) 5 pointsCreate New Form and Connect to Database 10 pointsCreate Add Member form, Add All Event Handlers and Code 10 pointsCreate All Buttons 5 pointsCreate SQL Query 10 pointsTotal 50 pointsRequired SoftwareVisual Studio 2012Use a personal copy or access the software at <a href="https://lab.devry.edu/" target="_blank" rel="nofollow noopener noreferrer">https://lab.devry.edu</a>.

<strong>Lab Steps</strong><strong>Step 1:Create New Application</strong>Create a new Windows application named Karate School Manager (see below). You will also need to download the project database from Doc Sharing entitled KarateDatabase.zip. Unzip this file to a convenient location. You will later add it to your project.

<strong>Step 2: Rename Startup Form</strong>Change the name of the startup form to MainForm.vb.

<strong>Step 3: Set Properties of Main Form</strong>Open MainForm and set the following properties.Size = 530, 275;Text = Karate School Manager;StartPosition = CenterScreen;MaximizeBox = False;FormBorderStyle = FixedSingle

<strong>Step 4: Insert Panel Control</strong>Insert a Panel control on the form and set its Size property to 390, 115. Insert another Panel control inside the first one and set its Size property to approximately 360, 80. Set the BorderStyle property of both panels to Fixed3D.

<strong>Step 5: Insert Label Control</strong>Insert a Label control inside the smaller panel and set its Text property to Kyoshi Karate School.

<strong>Step 6: Add Another Label Control</strong>Add another label control near the bottom of the form and set its Text property to Management System 1.0.

<strong>Step 7: Add MenuStrip Control</strong>Add a MenuStrip control to the form (make sure you have clicked the form, or the menu strip may be added to your panel) and insert the following menu items.&amp;File&amp;Exit&amp;Membership&amp;List All&amp;Find Member&amp;Add New Member&amp;Payments&amp;All&amp;One Member

<strong>Step 8: Add File | Exit Code</strong>Double-click the File | Exit menu item and insert the following code into its Click event handler.Me.Close()<strong>Step 9: Test File | Exit Menu Item</strong>Save the project and run the application. Verify that the form closes when you click the File | Exit menu item. Notice that the objects on the form have been centered (look under the Format menu for centering controls) and the text bolded and increased in size to be more readable. Maybe you will want to jazz it up a little more? Notice that the program is running with the File pull-down menu opened. The code window is in the background.

<strong>Step 10: Open Project</strong>Open the Karate School Manager project, if it is not already open.<strong>Step 11: Add AllMembers Form</strong>Go to the PROJECT | New Item pull-down menu and add a new form named AllMembersForm.vb to the project. Set its MinimizeBox and MaximizeBox properties to False. Set its Text property to All Members.

<strong>Step 12: Create Membership|ListAll Menu Item</strong>In MainForm, create a Click handler for the Membership / List All menu item and insert the following code.AllMembersForm.ShowDialog()<strong>Step 13: Add Data Source</strong>Now you will create and connect a database. Go to the View pull-down menu and select Other Windows – Data Sources or press Shift+Alt+D.

You’ll then see the Data Sources window. Click the Add New Data Source button.

Select Database and then Next.

Select Dataset and then Next.

Select the New Connection button.

Browse to wherever you downloaded your Karate data file and press OK.

It will then return to the Choose Your Data Connection window. Click Next.

It may ask you if you want to move the file. You can click No.

Let it save the connection string for you, then click Next.

Now check the Members table to add it to your dataset, which you should then name KarateDataSet.

You’ll now see the DataSource added.

You can close the Data Sources window at this time, or you can minimize it, leave it, drag and drop it onto another menu, or even drag and drop it onto another screen on your computer.<strong>Step 14: Add DataGridView Control</strong>Place a DataGridView control on the AllMembersForm and name it dgvMembers. Anchor the grid to all four sides of the form. Set the following property values: BackGroundColor = Control, BorderStyle = None, Row-HeadersVisible = False.

<strong>Step 15: Select Data Source</strong>Make sure you click the Data Grid one time to select it. A tiny arrow should appear in the upper right-hand corner. Click this arrow to expose the DataGridView Tasks menu.

Choose the Karate DataSet as your Data Source.

Check the Enable Editing and Enable Deleting check boxes only. If the grid’s column headings do not appear, edit the grid’s Columns property and use the arrow buttons next to the column names list to adjust the column order.

<strong>Step 16: Edit Column Properties</strong>1. Edit the Columns property from the Tasks menu.2. Select the Date_Joined column.3. Select DefaultCellStyle (you may have to scroll up).4. Click the “…” to change the style.

The CellStyle Builder will appear. Enter d into the Format property. This will format the date as a “short” date such as 3/7/2017. You can now exit the menus by clicking OK twice.

At this point, you will want to widen the size of the All Members form and the dgvMembers Data Grid to fit the data (see #1 below). Also note that by adding the data source, Visual Basic has added the proper <a href="http://ado.net/" target="_blank" rel="nofollow noopener noreferrer">ADO.NET</a> objects to the project (see #2 below).

<strong>Step 17: Add Close MenuItem</strong>Add a MenuStrip control to the form. Add a File menu item, with one subitem: Close. In the Close item’s Click handler, insert the Me.Close() statement.Step 18: Test Membership|ListAll Menu ItemSave the project and run the application. From the startup form menu, select Membership / List All. You should see a list of members.

<strong>Step 19: Create AddMember Form</strong>Add a new form to the project named AddMemberForm.vb. Set its Text property to Add New Member. Set the following property values: MaximizeBox = False; MinimizeBox = False; FormBorderStyle = FixedDialog.<strong>Step 20: Add Click Event Handler</strong>In MainForm, locate the Membership / Add New Member menu item; double-click the item and insert the following statement in its Click event handler.AddMemberForm.ShowDialog()Be sure to search for and read about the differences between using the Show() method and the ShowDialog() method.<strong>STEP 21: Setup KarateDataSet</strong>In the Data Sources window, locate the Members table under the KarateDataSet entry. Using the dropdown arrow to its right, select Details from the list.

<strong>Step 22: Create Data-Bound Fields</strong>Drag the Members table onto the form. Visual Studio should automatically create data-bound fields and a ToolStrip named MembersBindingNavigator. Set the Format property of the DateTimePicker control to Short.

<strong>Step 23: Remove Members Binding Navigator</strong>Delete the MembersBindingNavigator component from the form’s component tray. Open the form’s code window and delete the MembersBindingNavigatorSaveItem_Click method.

<strong>Step 24: Add Code for AddNew Event</strong>Replace the code in the form’s Load event handler with a statement that calls the following.AddNew.MembersBindingSource.AddNew()The statement clears the form’s input fields and waits for the user to enter data for a new member.<strong>Step 25: Add MenuStrip to Form</strong>Add a MenuStrip control to the form. Add a File menu item with one subitem: Close. In the event handler for the first item, insert a Me.Close() statement.<strong>Step 26: Create FormClosing Event</strong>Create a FormClosing event handler (see screenshot below).

Insert the following statement.MembersBindingSource.CancelEdit()

This statement cancels any edit operation that might be in progress. The user might have opened the form, begun to fill in the fields, changed his or her mind, and decided to close the form.<strong>Step 27: Configure DateTimePicker control</strong>Rename the DateTimePicker control to dtpDate. Add the following line to the form’s Load event handler.dtpDate.Value = TodayThis line is necessary to ensure that the date value will be saved in the database even if the user does not explicitly select a date.<strong>Step 28: Create Add Button</strong>Add a button to the form named btnUpdate. Set its Text property to Update. Create a handler for the button. It calls EndEdit to complete the add new row operation. Then it calls Update to save the DataSet modifications to the actual database. Finally, it closes the form as follows.TryMembersBindingSource.EndEdit()MembersTableAdapter.Update(KarateDataSet.Members)Me.Close()Catch ex As ExceptionMessageBox.Show(ex.Message, “Error”)End TryNotice that it uses a Try Catch statement to capture any errors occurring when trying to add to the database. Read about Try Catch statements if you have questions about how they work.<strong>Step 29: Test Add New Member</strong>Save the project and run the application. Click the Membership / Add New Member menu selection and add a new member. Choose a member ID that does not appear when you list all members. If you’re not sure, display a list of all members first.

<strong>Step 30: Create FindMember Form</strong>Add a new form to the project named FindMemberForm.vb. Set its properties as follows: Text = Find Member by Last Name; MaximizeBox = False; MinimizeBox = False; StartPosition = CenterScreen; FormBorderStyle = FixedDialog.<strong>Step 31: Add Code to Find Member Menu Item</strong>In MainForm, double-click the Membership / Find Member menu item and insert the following code in its event handler.FindMemberForm.ShowDialog()<strong>Step 32: Create Close SubMenu</strong>Open FindMemberForm in Design view, add a MenuStrip control to the form, and create a File submenu with one selection: Close. In its Click event handler, insert the Me.Close() statement.<strong>Step 33: Add LastName Label Control</strong>Add a Label control, a TextBox named txtLastName, and a Button named btnGo to the form.<strong>Step 34: Configure MembersTableAdapter</strong>Open the KarateDataSet.xsd file by double-clicking it in the Solution Explorer. Right-click the MembersTableAdapter, select Add, and then select Query.

Select Use SQL Statement as the command type.

Select the “SELECT which returns rows” query type.

Insert the following SQL query.SELECT ID, Last_Name, First_Name, Phone, Date_JoinedFROM MembersWHERE (Last_Name LIKE @name + ‘%’)After creating the SQL query, click the Next button.

In Choose Methods, select only the Fill a DataTable option and name the method FindMember.

Click Next and then Finish. You can now close the KarateDataSet.xsd file. Be sure to save it when you close it.<strong>Step 35: Configure DataGridView</strong>Place a DataGridView control on the form and name it dgvMembers. Set its properties as follows: BackGroundColor = Control; BorderStyle = None; Anchor = Bottom, Left, Right; RowHeadersVisible = False.<strong>Step 36: Setup Data Source</strong>Using the smart tag in the grid’s upper right corner, set its data source to the Members table of KarateDataSet. Disable adding, editing, and deleting of rows.

<strong>Step 37: Set Up FindMember Event</strong>Next, you will add a call to the Fill method in the event handler for the button that activates the search. Double-click the Go button and insert the following code in its event handler.‘ Perform a wildcard search for the last name.Me.MembersTableAdapter.FindMember(KarateDataSet.Members, txtLastName.Text)Normally, the Fill method has only one parameter: the DataSet’s table. But here you pass a second parameter, which is the value to be assigned to the query parameter.<strong>Step 38: Configure Accept Button Property</strong>Select the form with the mouse and set the Form’s AcceptButton property to btnGo. This will allow the user to press the Enter key when activating the search.<strong>Step 39: Clean up Load Event</strong>Remove any statements that might be inside the form’s Load event handler. (You don’t want the grid to fill with data until a member name has been entered.)Step 40: Test Find MemberSave the project and run the application. From the startup form, click Membership / Find Member from the menu. When the Find Member form appears, enter a partial last name, such as C or Ch, and click the Go button.

<strong>Step 41: Turn It In</strong>Zip up your entire project and the database. Submit it to the course Dropbox for Week 4. We will continue working on this project during Week 5.Top