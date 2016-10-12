# Scheduling Backups

- [Schedule Types](#types)
- [Creating a Schedule](#creating)

Schedules are reusable objects that control when group backups, custom event profile
email notifications, and policy-based replication occur.

Scheduled backups run automatically to ensure that backups occur on an ongoing basis.
You can schedule backups to run daily, weekly, or monthly. The scheduled backup can
include multiple clients or a single server.

1. Create a dataset to define the data that is included in the backups.
2. Create a schedule for when the backups should occur.
3. Create a retention policy to define how long to keep the backups in the system.
4. Create a group for the backups.
  - Assign the new dataset to the new group.
  - Assign a schedule to the new group.
  - Assign a retention policy to the new group.
  - Add one or more clients to the new group.
5. Enable scheduling for the group.

<a name="types"></a>
### Schedule Types

- **Daily** - Repeats a system activity every day at one or more times of the day. With daily
schedules, you must also limit the duration of the activity to prevent job overlap.
- **Weekly** - Repeats a system activity every week on one or more days of the week. With
weekly schedules, you must also define the earliest start time for the activity, as
well as the time at which the activity is stopped, even if it is still in progress.
- **Monthly** - Repeats a system activity on a specific calendar date or on a designated day of
the week each month, such as the first Sunday of every month. With monthly
schedules, you must also define the earliest start time for the activity, as well as
the time at which the activity is stopped, even if it is still in progress.
- **On-demand** - Defines a schedule that does not run automatically. This option is useful for
creating schedules that you can assign today but activate in the future. The option
is also useful to create schedules that are assigned to groups that only perform
on-demand backups, such as groups that contain only laptop clients.

<a name="creating"></a>
### Creating a Schedule

1. In Avamar Administrator, select Tools > Manage Schedules.
The Manage All Schedules window appears.
2. Click New.
The New Schedule dialog box appears.
3. In the Name box, type a name for the schedule.
Do not use any of the following characters in the name: ~!@$^%(){}[]|,`;#\/:*?<>'"&.
4. In the Repeat this schedule section, choose the schedule type:
  - Daily
  - Weekly
  - Monthly
  - On-Demand
5. Specify the schedule settings.
6. Ensure that the date and time listed next to Next Run Time near the top of the New
Schedule dialog box are correct.
7. Click OK.

