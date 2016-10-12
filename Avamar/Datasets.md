# Datasets

- [Source Data List](#source)
- [Exclusion and inclusion lists](#exclusion)
- [Processing relationship](#processing)
- [Unix Dataset](#unix)
- [Windows Dataset](#windows)
- [Creating a Dataset](#creating)

An Avamar dataset is a list of directories and files to back up from a
client. Assigning a dataset to a client or group enables you to save backup selections.

Each dataset defines:

- Source data list
- Exclusion list
- Inclusion list
- Plug-in options

<a name="source"></a>
### Source data list

Dataset definitions start with a source data list that consists of:

- Data from one or more plug-ins
- A defined file system hierarchy, either the entire file system or selected directories,
within each plug-in

<a name="exclusion"></a>
### Exclusion and inclusion lists

Datasets can also narrow the scope of the source data list by explicitly defining certain
directories and file types to exclude or include in each backup.

Because default dataset behavior is to include everything in the source data list, the
explicit exclusion and inclusion lists typically contain only a few entries.

When you specify exclusions and inclusions, case-sensitivity varies according to the
target computing platform for the backup. Exclusions and inclusions for Windows
platforms are not case-sensitive, while exclusions and inclusions for most other
platforms are case-sensitive.

<a name="processing"></a>
### Processing relationship

Avamar processes these dataset elements in the following order:

1. Source data—Source data from one or more plug-ins is defined. The default behavior
is to include all data from all defined plug-ins.
2. Exclusion list—Next, the exclusion list is used to eliminate certain directories and file
types from the dataset.
3. Inclusion list—Finally, the inclusion list is used to add back any files that were
eliminated from the dataset in the exclusion list.

<a name="unix"></a>
### Unix Dataset

The Unix Dataset is optimized for use with AIX, FreeBSD, HP-UX, Linux, and Solaris
clients. The initial settings in the Unix Dataset are:

- Only the AIX, FreeBSD, HP-UX, Linux, Macintosh OS X, and Solaris file system source
data plug-ins
- Explicit exclusion of various temp directories (/tmp, /var/tmp, /usr/tmp), core
dump files (core), and local cache files (*cache.dat, *scan.dat)
- No explicit inclusion list entries

The directories listed in the following table are also inherently excluded from all Unix
Dataset backups, even though they do not explicitly appear in the exclusion list.

<a name="windows"></a>
### Windows Dataset

The Windows Dataset is optimized for use with Microsoft Windows clients. The initial
settings in the Windows Dataset are:

- Only Windows file system source data plug-in
- No explicit exclusion or inclusion list entries

<a name="creating"></a>
### Creating a Dataset

1. In Avamar Administrator, select Tools > Manage Datasets.
The Manage All Datasets window appears.
2. Click New.
The New Dataset dialog box appears.
3. In the Name box, type a name for the dataset.
The name can include alphanumeric characters (A-Z, a-z, 0-9) and the following
special characters: period (.), hyphen (-), and underscore (_). Do not use Unicode
characters or the following special characters: ` ~ ! @ # $ % ^ & * ( ) = + [ ] { } | \ / ; : ' "
< > , ?
4. Click the Source Data tab, and then define the source data plug-ins that contribute
data to this dataset.
5. Click the Exclusions tab, and then define the data to exclude from the dataset:
  - Select the plug-in that you are using for the backups from the Select Plug-in Type list.
  - Type the path to the data to exclude, or click ... to browse to the data.
  - Click +.
  - Repeat these steps for each data path to exclude from the backups. Typical exclusion lists include /temp files and directories and UNIX core dumps.
6. Click the Inclusions tab, and then define the data to include in the dataset that
otherwise would be excluded based on the selections on the Exclusions tab:
  - Select the plug-in that you are using for the backups from the Select Plug-in Type
list.
  - Type the path to the data to include, or click ... to browse to the data.
  - Click +.
  - Repeat these steps for each data path to include in the backups.
7. Click the Options tab, and then set plug-in options either by using the graphical
controls or by typing option names and values as text entries.
The user guide for each plug-in provides details on the available options.
8. Click OK.


