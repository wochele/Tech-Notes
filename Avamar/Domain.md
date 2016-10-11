# Domains

Avamar client domains are distinct zones to organize and segregate clients in the Avamar
server. This provides enhanced security by enabling you to define administrative user
accounts on a domain-by-domain basis.

Avamar client domains are completely internal to the Avamar server and have nothing to
do with Internet domains.

### Creating a Domain

1. In Avamar Administrator, click the Administration launcher button.
The Administration window appears.
2. Click the Account Management tab.
3. In the left pane, select the location in the tree in which to create the domain.
4. From the Actions menu, select Account Management > New Domain.
The New Domain dialog box appears.
5. In the New Domain Name box, type the name of the domain.
Domain names must be 63 characters or fewer, and must not use any of the following
characters: =~!@$^%(){}[]|,`;#\/:*?<>'"&.
6. (Optional) Type the name, telephone number, email address, and location for a
contact for the domain in the remaining fields on the New Domain dialog box.
7. Click OK.
A confirmation message appears.
8. Click OK.

### Edit a domain

1. In Avamar Administrator, click the Administration launcher button.
The Administration window appears.
2. Click the Account Management tab.
3. In the tree, select the domain to edit.
4. From the Actions menu, select Account Management > Edit Domain.
The Edit Domain dialog box appears.
5. Edit the domain contact information.
6. Click OK.
7. Click OK on the confirmation message that appears.

### Deleting a domain

When you delete a domain, the process also deletes any clients in the domain. To
preserve the clients in the system, move the clients to a new domain before you delete
the domain.

In addition, if you use directory service authentication, then Avamar removes the LDAP
maps that use that domain for access. The associated directory service groups are
otherwise unaffected by the deletion.

1. (Optional) Move any clients in the domain to a new domain. Moving a client to a new
domain on page 59 provides instructions.
2. In Avamar Administrator, click the Administration launcher button.
The Administration window appears.
3. Click the Account Management tab.
4. In the tree, select the domain to delete.
5. From the Actions menu, select Account Management > Delete Domain.
A confirmation message appears.
6. Click Yes.
7. Click OK on the second confirmation message that appears.
