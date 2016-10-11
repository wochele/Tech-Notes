# Client Management

### Register client in Avamar Administrator

1. In Avamar Administrator, click the Administration launcher button.
The Administration window appears.
2. Click the Account Management tab.
In the Account Management tree, the icons for the clients indicate status. An x
appears for disabled clients, a question mark appears for unregistered clients, and
there is no special icon designation for active clients.
3. In the tree, select the domain for the new client.
4. From the Actions menu, select Account Management > New Client.
The New Client dialog box appears.
5. From the Client Type list, select Normal.
6. In the New Client Name field, type the client name.
7. (Optional) Type the client contact name, telephone number, email address, and
location in the remaining fields of the New Client dialog box.
8. Click OK.
A confirmation message appears.
9. Click OK.

### Install Windows Client

![client install](Pics/Avamar-Client-Install-01.png)

![client install](Pics/Avamar-Client-Install-02.png)

![client install](Pics/Avamar-Client-Install-03.png)

![client install](Pics/Avamar-Client-Install-04.png)

![client install](Pics/Avamar-Client-Install-05.png)

![client install](Pics/Avamar-Client-Install-06.png)

![client install](Pics/Avamar-Client-Install-07.png)

### Activating a client

Client activation is the process of passing the client ID (CID) back to the client, where it is
stored in a file on the client file system.

##### Before you begin

- The client must be present on the network.
- The Avamar client software must be installed and running on the client.
- The Avamar server must be able to resolve the hostname that was used to register the
client.

##### There are two ways to activate a client:

- Initiate activation from the client. The EMC Avamar Backup Clients User Guide describes
this method.
- Invite the client to activate with the server by using Avamar Administrator.

NOTICE

HP-UX, Linux, and Solaris clients can either be activated during installation or by using
Avamar Administrator. There is no client-side command to initiate client activation on
these computing platforms.

Procedure

1. In Avamar Administrator, click the Administration launcher button.
The Administration window appears.
2. Click the Account Management tab.
In the Account Management tree, the icons for the clients indicate status. An x
appears for disabled clients, a question mark appears for unregistered clients, and
there is no special icon designation for active clients.
3. In the tree, select the client to activate.
4. From the Actions menu, select Account Management > Invite Client.
A status message indicates that the client was sent an invitation to activate with the
server.
5. Click OK.

- Once this is complete, the client should be in the Avamar Administrator
