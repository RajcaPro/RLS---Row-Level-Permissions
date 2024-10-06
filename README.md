# RLS---Row-Level-Permissions
----------
In today's post, we will look at two important aspects of access management: granting access to a single report and to a workspace. We will also discuss the differences between these two methods and the required permissions needed to grant such access.

Let's start by asking the most important question: what high-level permissions do I need in a workspace to assign roles to other users?
The answer is simple: to grant access to a workspace to other users, you must have the "Administrator" role in that workspace. This is a key point because without this role, you won't even see the options for the permissions section.

There is one more important thing!

To have the Administrator role in a Power BI workspace, the user must have a Power BI Pro subscription or use Power BI Premium.

If the workspace is set to use Power BI Premium, the workspace Administrator must have a Pro license to manage members and access. However, other users can access the content without having a Pro license as long as they are in the workspace.

But don’t worry! Users who are using the Power BI Pro trial can also serve as the workspace Administrator, at least for some time.

--------------------

Now we can move on to the next part and briefly discuss the available roles and their capabilities.

Available roles in a workspace:

Administrator (Admin): Full control over the workspace. Can manage users and their permissions, edit, and delete resources.

Member: Can create, edit, and delete reports but does not have access to manage users.

Contributor: Can edit reports and datasets but does not have access to manage the workspace.

Viewer: Can only view reports and other resources without the ability to edit.


-----------

With the above knowledge, we can now focus on granting permissions to the workspace!

Steps to grant access to a workspace:

1) Log in to Power BI Service.

2) Go to the workspace where you want to grant access.

![image](https://github.com/user-attachments/assets/3e788f9a-ad0c-43cb-bb6a-e6af13fa0cd2)

3) Click on the Manage Users icon or Members.

![image](https://github.com/user-attachments/assets/cc65af7b-c318-4768-ad6f-1acd0d7e798d)

4) Add a new user by entering their email address.

![image](https://github.com/user-attachments/assets/0179fb23-6d2d-499d-aa33-13318539f0a4)

5) Specify what permissions they should receive:

Administrator (Admin): Full access to all features, including the ability to grant permissions to others.
Member: Can edit and share the content of the workspace, but does not have full administrative control.
Contributor: Can edit content (e.g., reports and dashboards) but cannot manage the workspace or grant permissions.
Viewer: Can only view the content of the workspace, with no ability to edit or create new resources.

Remember!!!
To grant access to other users in the workspace, you must have the Administrator role in that workspace.



-----------------

Great! Now we know how to add users to a workspace!!!

But what if we don’t want users to have access to the entire workspace, only to view a single report?
There’s a solution for that! :)

Steps to grant access to a report:

1) Log in to Power BI Service.

2) Go to the report you want to share.

![image](https://github.com/user-attachments/assets/6eb77676-c0d2-471c-8db4-1887a2919fc2)

3) Click the Share button.

4) Enter the email address of the user or group you want to grant access to.

![image](https://github.com/user-attachments/assets/f79b9ff2-fed8-4a4f-b771-fcb01098b256)

5) Specify the access level: the ability to view (view) the report or additional options, such as editing (edit), if available.

![image](https://github.com/user-attachments/assets/d4af1da7-69e2-41a6-9793-9cd720c1d8dc)

(Optional) You can add a message and send a notification to the user!

Available permissions for the report:

View: The user can only view the report and cannot edit it.

Reshare: Allows the user to share the report with other users if this option is enabled.

Build: Users with this permission can create new reports based on the dataset from this report.

To share reports with other users, you must have one of the following permissions:

- Owner of the report

- Administrator of the workspace where the report is located

- Member of the workspace with permission to edit reports.


---------------

Let's move on to the final step, which is granting row-level permissions. ✨✨

Imagine that in our company, we have several sales directors, and each of them is assigned to their own network of stores. Our main goal is to block the report for the sales director who selected the wrong network of stores (meaning one they do not manage). We don't want them to have access to data that isn't theirs. Another requirement is that the CEO should have access to all data, meaning all networks of stores, so they can monitor the performance of the sales directors.

It seems a bit complicated, right?
I assure you that after this post, everything will become clear! :) ✨🚀

To grant access to a workspace or a selected report, we had to work in the Power BI app.
To add row-level permissions, we need to work from Power BI DESKTOP!!!

Let’s get started!

In the first step, we go to Model View:

![image](https://github.com/user-attachments/assets/de7f3171-01ec-4c3a-8d1d-19973cff1524)

Next, in the right panel of the page, select the MODEL section.

![image](https://github.com/user-attachments/assets/83fcbef5-7ab7-4809-8f79-7d99aa25a87f)

We look for the Roles section and click on Manage roles.

![image](https://github.com/user-attachments/assets/9762bddb-d6c7-4b23-935e-24162cfafcb6)

Result

![image](https://github.com/user-attachments/assets/d513e814-da37-4d03-ab1d-82e67234c93b)

We add a new role and name it XXX:

![image](https://github.com/user-attachments/assets/b8bcdd07-9558-4883-9f9b-6f9c7b988a68)

We select the table on which the permissions will apply, and in our case, the level of permission will be based on the first and last name of the sales director.


![image](https://github.com/user-attachments/assets/e32d6cc5-ce97-4867-8909-0fc191a4059c)


![image](https://github.com/user-attachments/assets/2185fe19-fa71-49ee-8f78-babc583a3f95)

We select to make the column First and Last Name equal to the name of our sales director.

![image](https://github.com/user-attachments/assets/7ca027ee-9e33-4da3-8089-dc96fee7096b)

Now that we have done that, there is just one task left!!!

We go back to the Power BI app to our workspace and select the data source for our report.

![image](https://github.com/user-attachments/assets/7592286a-d9db-447a-93a3-e9de214d51d5)

In this section, we can see a list of our sales directors and a list of people who have access to their data!!!

![image](https://github.com/user-attachments/assets/91ca0811-615c-4cf9-81be-d0cbb920dd8b)





That’s the end of this post!

I hope you will use it in your work 🚀

Best Regards, Mateusz Rajca







