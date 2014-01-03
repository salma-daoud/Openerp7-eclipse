Openerp7-eclipse
================

Setup eclipse for OpenERP 7 
This is a tutorial about how to use eclipse as a developping and debugging environnement for openERP 

INSTALLATION
============
1- Download/install « Openerp-allinone-setup-7.0-latest.exe », in order to install all required packages then we stop openERP service and then set the boot parameter to "manual"
Computer-->manage-->application and services --> services --> Openerp7 --> stop and set the boot paramaeter to manual
Installer Python-2.7.3.msi

DEPENDENCE
==========

Install Babel-0.9.6.win32.exe
Install Lxml-2.2.8.win32-py2.7.exe
Install PIL-1.1.7.win32-py2.7.exe
Install Pywin32-217.win32-py2.7.exe
Install Psycopg2-2.4.5.win32-py2.7-pg9.1.3-release.exe
Install Py2exe-0.6.9.win32-py2.7.exe
Install Python-ldap-2.4.7.win32-py2.7.msi
Install PyXML-0.8.4.win32-py2.7.exe
Install Setuptools-0.6c11.win32-py2.7.exe

ECLIPSE
=======

Create the Workspace (C:\Users\MyUSERNAME\workspace\)
Install Pydev -> Help -> Install new Software
Add -> (Name : Pydev -> Location : http://pydev.org/updates/
unzip openerp-7.0-latest.tar.gz in the  Workspace (C:\Users\MyUSERNAME\workspace\openerp-7.0)
Clic  -> New -> PyDev Project -> Project Name: « openerp-7.0″ -> Finish
setup.py -> Run as -> Run configuration

In eclipse go to Menu "Run/Debug Configurations". In configuration window under "Python Run", create new debug configuration(Double click on 'Python Run').

3: After creating new debug configuration follow the given steps:

3.1: In "Main" tab under "Project", select the "server" project or folder (in which Openerp Server resides) from your workspace.

3.2: Write location of 'openerp-server' under "Main Module".

Ex: ${workspace_loc:server/openerp-server}.
3.3: In "Arguments" tab under "Program Arguments", click on button "Variables" and new window will appear.

3.4: Then create new "Variable" by clicking on "Edit Variables" button and new window will appear.

3.5: Press on "New" button and give your addons path as value.

addons = ../addons (the path to openerp/addons)
db_host = False
db_port = False
db_user = openpg
db_password = openpgpwd
3.6: Press Ok in all the opened windows and then "Apply".

4: Now into "PyDev Package Explorer" view go to 6.1/server and right click on "openerp-server" file, Select 'Debug As --> Python Run'.

5: Now in "Console" you can see your server has been started.

