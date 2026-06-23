# Starting a Jupyter Notebook Session on Hyak's Open OnDemand Platform 

Connect to University of Washington's OnDemand services for Hyak by directing your browser to this link: 

**https://ondemand.hyak.uw.edu/**

You will be asked to sign in with your UWNetID and password. 

![capture of UW's login interface](screenshots/uwnetid-sign-in.png 'login')

After that, you will be prompted to authenticate with 2-Factor Authentication. Which will look something like the following:

![capture of Duo 2 factor authentication](screenshots/duo-push.png '2FA')

After that is complete, you will see the opening message as below: 

![capture of Open OnDemand Home](screenshots/ood-home.png 'home')

We will review other features available to you in other workshops during this REU. To proceed with our task, we will click the menu option "Interactive Apps" and select Jupyter:

![capture of interactive applications drop-down menu](screenshots/interactive-apps.png 'apps')

A formula request will be the next screen. Please change the fllowing fields:

* Account change to "memc"
* Parition change to "compute"
* Jupyter Container change to "Module/jupyter-minimal"
* Memory change to "30"
* Number of Hours change to "3"
* Finally make sure the "JupyterLab" option is selected

Push the "Launch" button to request the Jupyter Session.

![capture of the jupyter job request form](screenshots/job-request.png 'request')

The request might wait in the queue for resources to be allocated, but shortly, there will be a button that says "Connect to Jupyter" click it to open JupyterLab. 

![capture of the running jupyter job and button to connect](screenshots/connect-jupyter.png 'connect')

A new tab will open with your JupyterLab session, and look something like the below: 

![capture of jupyter lab](screenshots/jupyterlab.png 'lab')

Here the left sidebar is a view of you Home directory on Hyak's third generation cluster called `klone`. As you create Jupyter Notebooks, they will be appear here or inside of a subdirectory. We'll talk more about this soon. 

The panel on the right shows choices of the type of Notebook you can open. For this tutorial, we will be using the `datascience`. Go ahead an click on the `datascience` kernel under the Notebook section as shown in Red. 

If a kernel selection window prompts, make sure “datascience” is selected, then click Select.

You have just started your first Jupyter Notebook of this workshop titled "Untitled.ipynb". The file extension ".ipynb" is the standard extension for ipykernel notebooks, but we can give our Notebook a name. Right click on the "Untitled.ipynb" tab and select "Rename Notebook..." and choose a new name for it. 

![capture showing how to rename the notebook](screenshots/rename-nb.png 'rename')

Now you are ready to learn some Python. 

Your session will automatically end after 3 hours (or your selected time limit), but you can end your session early by closing the window showing JupyterLab, and finding the OnDemand service window showing your running Jupyter Session. Use the Delete button to end your session manually. 

![capture showing the button to delete or cancel the jupyter job](screenshots/delete-session.png 'cancel')