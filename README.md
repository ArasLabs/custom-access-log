# Custom Access Log

This project adds functionality to log View Form operation for any items: When, Who, What　items were viewed.

Administrator easily can view the access logs as a list and can get statistical information from the logs by standard Simple Search.
e.g. 
- Total Item view count for each items.
- Total Item view count for each users.

## History

This project and the following release notes have been migrated from the old Aras Projects page.

Release | Notes
--------|--------
[v1](https://github.com/ArasLabs/custom-access-log/releases/tag/v1) | Build 1 is the first version. Instructions are described in the [ReadMe.pdf](../Documentation/AccessLogPackage-ReadMe-Japanese.png).

#### Supported Aras Versions

Project | Aras
--------|------
[v1](https://github.com/ArasLabs/custom-access-log/releases/tag/v1) | 9.4, 10.0

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed
2. Aras Package Import tool
3. **CustomAccessLog** import package

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\Imports\00.core1(root)\imports.mf` file in the Manifest File field.
6. Select all in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Repeat Steps 5-8 for the following import paths:
  - `..\Imports\01.core2(root)\imports.mf`
  - `..\Imports\02.function(admin)\imports.mf`
10. Close the Aras Package Import tool.

## Usage

1. Log in to Aras as admin.
2. Navigate to **Administration > ItemTypes** in the TOC and search for the ItemType you would like to enable custom access logging on.
3. Open the ItemType for editing.
4. Check off the **Access Log Tracking** checkbox.
5. Save, unlock, and close the ItemType.

You can view the collected logs via **Administration > Access Log** in the TOC.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Credits

Created by NEOSYSTEM Co.,Ltd.
