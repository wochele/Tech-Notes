# Groups

- [VMware Groups](#vm)
- [Creating a Group](#create)
- [Managing Group Membership](#manage)

Avamar uses groups to implement various policies to automate backups and enforce
consistent rules and system behavior across an entire segment, or group, of the user
community.

### Group members

Group members are client machines that have been added to a particular group for the
purposes of performing scheduled backups. Because the normal rules for domain
administrators apply, these clients must be located within the same domain or within a
subdomain of where the group exists.

###Group policy

When you create a group, you specify the dataset, schedule, and retention policy for the
group. These three objects comprise the **group policy**. The group policy controls backup
behavior for all members of the group.

You can override group dataset and retention policy settings for a client by making
explicit dataset or retention policy assignments for the client. However, schedules apply
only to groups, not individual clients.

<a name="vm"></a>
### VMware Groups

- Default Proxy Group
  - The Default Proxy Group is the default group for VMware Image Proxy clients.
You cannot delete the Default Proxy Group. Enabling the Default Proxy Group
does not conflict with scheduled backups performed by other plug-ins
configured on the proxy client.
- Default Virtual Machine Group
  - New virtual machine clients are automatically added to the Default Virtual
Machine Group when they are registered. You cannot manually delete the
Default Virtual Machine Group, but it is automatically deleted if you delete
the vCenter domain.
- VM Backup Validation groups
  - VM Backup Validation groups are used to implement the restore rehearsal
feature for VMware virtual machines.

<a name="create"></a>
### Creating a Group

When you create a group, you define the dataset, schedule, and retention policy, which
together comprise the group policy for scheduled backups of all members of the group. A
group must contain at least one Avamar client. If the group contains two or more clients,
then the clients must belong to the same Avamar domain. You can override group policy
settings at the client level.

1. In Avamar Administrator, click the Policy launcher button.
The Policy window appears.
2. Click the Policy Management tab.
3. Click the Groups tab.
4. Select the domain for the group.
The Policy window displays a table that contains groups for the domain.
5. Select Actions > Group > New > Backup Group.
The New Group wizard appears.
6. Type a name for the new group in the Name box.
The name can include alphanumeric characters (A-Z, a-z, 0-9) and the following
special characters: period (.), hyphen (-), and underscore (_). Do not use Unicode
characters or the following special characters: ` ~ ! @ # $ % ^ & * ( ) = + [ ] { } | \ / ; : ' "
< > , ?
7. Clear the Disabled checkbox to use this group for scheduled client backups.
Selecting the checkbox disables backups for the group.
8. From the Avamar encryption method list, select an encryption method to use for data
transfer between the Avamar server and the client during the backup.
The encryption technology and bit strength for a client/server connection depends on
several factors, including the client operating system and Avamar server version. The
EMC Avamar Product Security Guide provides additional information.
9. (Optional) Select Override Schedule to override the assigned schedule for this group:
  - To skip the next scheduled backup, select Skip Next Backup.
  - To perform the next scheduled backup one time only, select Run Next Backup
Once.
10. Click Next.
The next New Group wizard page appears with dataset information.
11. From the Select An Existing Dataset list, select the dataset that you created, and then
click Next.
The next New Group wizard page appears with schedule information.
12. Select a schedule from the Select An Existing Schedule list, and click Next.
The next New Group wizard page appears with retention policy information.
13. Select a retention policy from the Select an Existing Retention Policy list, and click
Next.
The final New Group wizard page appears. A list of domains appears in the Choose
Domain pane.
14. Select the domain for the client.
A list of Avamar clients appears in the pane below the Choose Domain pane.
15. Select the checkbox next to the clients to include in the group.
The clients appear in the Members pane.
16. (Optional)To remove a client from the group, select the client from the Members list,
and then click the red X.
17. Click Finish.

<a name="manage"></a>
### Managing Group Membership

You can manage group membership in Avamar Administrator either by adding or
removing members for a group or adding or removing groups to which a client belongs.

The method that you use to manage group membership depends on the situation. For
example, if you are adding or deleting multiple clients from a single group, then the
group-centric method is efficient. Conversely, if you are adding or removing a single client
from multiple groups, then the client-centric method is most efficient.
