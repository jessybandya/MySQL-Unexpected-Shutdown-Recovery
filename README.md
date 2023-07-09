# MySQL Unexpected Shutdown Recovery

If you encounter an unexpected shutdown of MySQL in XAMPP, you can follow these steps to recover your databases using the MySQL backup folder included with XAMPP.

## Instructions

1. Rename the `mysql/data` folder: 
   - Locate the `mysql/data` folder within your XAMPP installation directory.
   - Rename the `data` folder to `data_old` or any other name of your choice.

2. Make a copy of the backup folder:
   - Locate the `mysql/backup` folder within your XAMPP installation directory.
   - Make a copy of the entire `backup` folder.

3. Rename the copied backup folder:
   - Rename the copied `backup` folder to `data`. This will replace the original `data` folder that you renamed in Step 1.

4. Restore databases from the old data folder:
   - Open the `data_old` folder that you renamed in Step 1.
   - Copy all the database folders within `data_old` except for the `mysql`, `performance_schema`, and `phpmyadmin` folders.
   - Paste these database folders into the new `data` folder that you created in Step 3.

5. Copy the `ibdata1` file:
   - Locate the `ibdata1` file within the `data_old` folder.
   - Copy the `ibdata1` file.
   - Paste the `ibdata1` file into the new `data` folder.

6. Start MySQL:
   - Open the XAMPP control panel.
   - Start the MySQL module from the control panel.

By following these steps, you should be able to recover your databases from the backup folder and start MySQL in XAMPP again.

Please note that it's always recommended to regularly backup your databases to prevent data loss in case of unexpected shutdowns or other issues.

## Directory Structure

Your XAMPP installation directory should have the following structure:

