# Retention

- [Advanced Retention Settings](#advanced)
- [Creating a Retention Policy](#policy)

Backup retention policies enable you to specify how long to keep a backup in the system.

A retention policy is assigned to each backup when the backup occurs. Specify a custom
retention policy when you perform an on-demand backup, or create a retention policy
that is assigned automatically to a group of clients during a scheduled backup.

When the retention for a backup expires, then the backup is automatically marked for
deletion. The deletion occurs in batches during times of low system activity.

If required, you can manually change the retention setting for an individual backup that
has already occurred. Changing the retention type for a backup on page 117 provides
instructions. If you change a configured retention policy, however, the change applies
only to backups that occur after the change. The retention setting remains the same for
backups that have already been performed. Therefore, it is important to consider and
implement the best retention policy for a site before too many backups occur.

There are two types of retention settings:

- Basic retention settings specify a fixed expiration date.
- Advanced retention settings specify the number of daily, weekly, monthly, and yearly
backups to keep.

<a name="advanced"></a>
### Advanced Retention Settings

With advanced retention settings, it is possible to assign the expiration of backups
dynamically by using the number of daily backups, weekly backups, monthly backups,
and yearly backups to retain in the system.

For scheduled daily backups, some backups are automatically assigned an advanced
retention type:

- The first successful scheduled backup each day is designated as the daily backup.
- The first successful scheduled backup each week is designated as the weekly
backup.
- The first successful scheduled backup each month is designated as the monthly
backup.
- The first successful scheduled backup each year is designated as the yearly backup.

For assigning advanced retention types, each day begins at 00:00:01 GMT, each week
begins on Sunday, each month begins on the first calendar day of that month, and each
year begins on January 1.

<a name="policy"></a>
### Creating a Retention Policy

1. In Avamar Administrator, select Tools > Manage Retention Policies.
The Manage All Retention Policies window appears.
2. Click New.
The New Retention Policy dialog box appears.
3. In the Name box, type a name for the retention policy.
Do not use any of the following characters in the retention policy name: ~!@$^%(){}
[]|,`;#\/:*?<>'"&.
4. Complete the steps for either basic retention settings or advanced retention settings.
  - Advanced
    - Select Override basic retention policy for scheduled backups.
    - Click Advanced. The Edit Advanced Retention Policy dialog box appears.
    - Specify the maximum number of daily, weekly, monthly, and yearly backups to retain.
    - Click OK on the Edit Advanced Retention Policy dialog box.
5. Click OK on the New Retention Policy dialog box.
