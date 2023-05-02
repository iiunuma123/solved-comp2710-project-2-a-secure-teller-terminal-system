Download Link: https://assignmentchef.com/product/solved-comp2710-project-2-a-secure-teller-terminal-system
<br>
<strong><em><u>Design Portion:</u></em></strong>

Create a Word or PDF file named “Project2 Design”. Please submit a Word (.doc) or PDF

(.pdf) file.

<em><u>Process (Steps 1-3 due with design portion, Steps 4-5 due with programming portion):</u> </em>Each of the following should address the program specification below. Concern yourself more with thinking about the problem than worrying about the specifics of implementation at this stage. For the design portion turn-in, you will provide Steps 1-3. For the programming portion (final) turn-in, you will provide <strong>all the steps</strong> (including any revisions you may have made). Please note revisions in your final copy. You should provide:

<ol>

 <li><strong>Analysis :</strong> Write a few important use cases (at least three). These use cases describe how the user interacts with a teller terminal system (what they do, what the system does in response, etc.). Your use cases should have enough basic details such that someone unfamiliar with the system can have an understanding of what is happening in the teller terminal. They should not include internal technical details that the user is not (and should not be) aware of. Make sure that any special rules/features you plan to add are clearly described in your Analysis section.</li>

</ol>

<strong> </strong>

<ol start="2">

 <li><strong>Design</strong> From your use cases, identify likely candidates for software objects. Construct a <strong>Class Diagram</strong> for the objects you identified for this project. Each class should have the following:</li>

</ol>

<ul>

 <li>The name and purpose of the class</li>

 <li>The member variables and the functions of the class</li>

 <li>Any other classes that this class depends on or uses</li>

 <li>Any relevant notes that do not fit into the previous categories</li>

</ul>

<ol start="3">

 <li><strong>Testing (10 points)</strong>: Develop lists of specific test cases (at least three):</li>

</ol>

For the system at large. In other words, describe inputs for “nominal” usage. You may need several scenarios. Also, suggest scenarios for abnormal usage and show what your program should do (for example, entering a negative number for a menu might ask the user to try again). Remember, test cases are specific, repeatable, and should have a clearly defined result.

<strong><em><u>Program Portion:</u></em></strong><em>  </em>

<ol start="4">

 <li><strong>Implement your solution in C++ (65 points).</strong></li>

</ol>




<ol start="5">

 <li><strong>Test Results (5 points)</strong>: <strong><em>After developing the teller terminal system</em></strong>, actually try all of your test cases. Show the results of your testing (a copy and paste from your program output is fine – do not stress too much about formatting as long as the results are clear). You should have test results for every test case you described. If your system does not behave as intended, you should note this</li>

</ol>

<strong><em><u>Program:</u></em></strong><em>  </em>

Write a program called Project2.cpp. Use comments to provide a heading at the top of your code containing your name, Auburn Userid, and filename. Please describe any help or sources that you used.

<em><u>Background: Building a Secure Teller Terminal System</u> </em>

In this project, you will design and develop a secure teller terminal system for the Auburn branch of Tiger Bank, which comprises multiple branches in the State of Alabama. After the development of the secure teller terminal system, the system will be widely used in other branches of Tiger Bank. The Auburn branch manages a number of Tiger bank’s accounts. Each account contains a unique account number, a balance, as well as other important information. Once you complete this project, your terminal system at each Tiger Bank branch will be connected. In this project, you only will be focusing on the <em>design and implementation of teller terminals</em> for Tiger Bank. A teller terminal system to be developed is a standard PC application which handles local transactions. All human interaction with the teller terminal is through a keyboard. Other specialized input devices like smart-card readers are not considered a cost-effective option for our project.

Staff at the Auburn branch access account information and customer data through the teller terminal system to be developed by you. In this project, let us refer to this information as <em>client data</em>. Client data must be carefully controlled in order to improve the security of the teller terminal system. Whether a given Auburn branch employee is permitted to access any particular piece of client data depends on the employee’s job level.

In this prototype system, there are two types of users in the system – system administrators and branch staff. Any system administrator can add a new branch staff member to access the system or delete existing staff members from the system (see sample usage 2.1, 2.2, and 2.3). Branch staff identifiers used in this system are called <em>user name</em>.

Your teller terminal system must <strong>authenticate</strong> each access request to the system. You will implement a mechanism to authenticate requests made at the teller terminal.

A teller terminal is either in the <em>idle</em> state or the <em>active</em> state. In what follows, we summarize the behaviors of the teller terminal in these two states.

<ul>

 <li><strong>In the Idle State: </strong></li>

</ul>

An idle teller terminal displays a <strong><em>login menu </em></strong>(see Sample Usage 1). It invites a branch employee to enter a userid and password and either (i) to manage client and account information or (ii) add/delete a user (branch staff) if the user is a system administrator or (iii) to change his/her password (in which case, the teller is first authenticated using the current password, then the password is updated, and finally a session is initiated with the authenticated teller). In all the cases, the information provided is checked for validity. If the user name and password are valid, then the teller terminal system is placed in the active state and a session is started.

<ul>

 <li><strong>In Active State: </strong></li>

</ul>

For system administrators, an active teller terminal displays a “System Administration” main menu that invites an administrator to manage information of branch staff members, clients, and accounts (see sample usage 2.1) or change password.

For branch staff, an active teller displays a “Branch Staff” main menu that invites a branch staff member to manage client and account information or change password (see sample usage 3.2).

<em><u>Design and Implementation Requirements</u>  </em>

1. System Login (see sample usage 1 and 2)

The teller terminal displays a <strong>login menu </strong>(see Sample Usage 1. Login). It invites a branch employee to enter a userid and password. If the user name and password are valid, then the teller terminal system is placed in the active state and a session with the teller terminal is started.

1.1 Login as a system administrator (see sample usage 1)

A system administrator can (i) manage client and account information, (ii) add/delete/display users (branch staff members), and (iii) change his/her password.  When a system administrator login to the system, the administrator can choose to do the following:

<ul>

 <li>Client and Account Management</li>

 <li>Add a branch staff member</li>

 <li>Delete a branch staff member</li>

 <li>Display branch staff q Change password</li>

</ul>

<h2>1.2 Default system administrator and password (see sample usage 1)</h2>

When the system is running for the first time, there is only a <strong><u>default system administrator</u></strong> – named “admin” – in the system. The <strong><u>default password</u></strong> of the default administrator is initially set to be <strong>0000</strong>. Of course, this password can be changed later. Initially (i.e., before the first run), there is no system administrator and branch staff except the default administrator. Thus, only admin can use 0000 as the password to access the system.

1.3 Login as a branch staff member (see sample usage 3)

When a branch staff member logs in the teller terminal, the staff can perform the following two tasks:

<ul>

 <li>Client and Account Management</li>

 <li>Change password</li>

</ul>

<h2>1.4 Change password (see sample usage 2.4)</h2>

Regardless of the user’s role, the user is first authenticated using his/her current password. Then, the password is updated. A changed password is valid only if (i) it is not equal to the old password and (ii) it is a non-empty password.

<h1>2. System administration management</h1>

<h2>2.1 Add branch staff to the system: (see sample usage 2.1)</h2>

A system administrator can add new users (branch staff members) to the teller terminal system. When a new user is added into the teller system by the system administrator, user name and password of the new staff member must be initialized. <strong>Empty value of the user name or password is not acceptable.</strong>

Display branch employee: (see sample usage 2.2)

User names and roles of all the branch employees including administrators are displayed. Before displaying a list of employees, the total number of employees must be displayed. You can simply follow the format below:

There are 3 users in the system.

<ol>

 <li>User Name: admin     Role: System Administrator</li>

 <li>User Name: abc0002 Role: System Administrator</li>

 <li>User Name: xyz0003 Role: Branch Staff  Press any key to continue…</li>

</ol>

<h2>Delete a branch staff: (see sample usage 2.3)</h2>

To delete a branch staff member from the teller terminal system, a system administrator must login to the system and use the system administration menu. The system administrator must use a user name to identify which staff should be deleted. After the administrator enters the staff member’s user name, the administrator needs to confirm this deletion. Sample user interface is given below:

Delete a user – User Name: <strong>abc0005</strong>

1) Confirm 2) Cancel

Please choose an option: <strong>1 </strong>

The system will first search the list of staff for the staff to be deleted. If the staff member’s information is not in the system, a warning message (see the sample warning message below) will pop up.

Warning – User abc0005 is not in the system. No user is deleted!

<h1>3. Client and Account Management</h1>

<h2>3.1 Add a client (see sample usage 4.2)</h2>

If “Add a client” is selected, the new client’s name, address, social security number, employer, and annual income must be entered. For simplicity, we assume that client names are unique, meaning that we can use client names as client identifiers.

Add an account (see sample usage 4.3)

If “Add an account” is selected, a client’s name must be entered first. If the client is not found in the system, an error message will pop up. If the client is in the system, then the branch staff member has to enter account number, account type, and account balance.

Edit client information (see sample usage 4.4)

If “Edit Client Information” is selected, a client’s name must be entered. If the client is not found in the system, an error message will pop up. If the client is in the system, then the branch staff can edit the client’s information, including address, social security number, employer, and annual income. Before updating the client’s information, existing client information is displayed. If the branch staff selects “Confirm”, the client information can be updated. <strong>Note</strong>: In this prototype, clients cannot be deleted. We also assume that client names should not be changed because we use client names as IDs.

Manage an account (see sample usage 4.5)

If “Manage an account” is selected, an account number will be entered. If the account does not exist in the system, an error message will pop up. The format of the error message is given below:

Error – Account &lt;Account_Number&gt; is not in the system!

After the account is chosen, the staff can either deposit or withdraw funds by choosing a menu option. Thus, if the account exists in the system, the following menu will appear:




Manage account &lt;Account_Number&gt; for &lt;Client Name&gt; …

<ul>

 <li>Deposit</li>

 <li>Withdraw</li>

 <li>Cancel</li>

</ul>

<h2>Save client and account information (see sample usage 4.6)</h2>

If “Save Client and Account Information” is selected, then the Teller Terminal System writes all current accounts to a file called “account-info” and writes all client information to a file called “client-info”. Each time the teller terminal is started; the “account-info” and “client-info” files containing the account and client information are loaded and initialized. For simplicity, the names of the two files are pre-specified. Branch staff employees are not authorized to change the file names.

<h1>4. System Quit</h1>

This command should safely terminate the system. Information of a list of system administrators and branch staff (i.e., user names, passwords, roles) must be saved to a file called “staff”.

<h1>5. Usability concerns and error-checking</h1>

Your program’s output does not necessarily need to match the style of the sample output, but the contents should be understandable and no functionality should be missed. You should appropriately prompt your user and assume that they only have basic knowledge of the system. You should provide enough error-checking that a moderately informed user will not crash your program.