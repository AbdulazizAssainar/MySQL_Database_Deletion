# MySQL_Database_Deletion

1. **Open Command Line:**
   Open your command line interface.

2. **Log in to MySQL:**
   Type the following command and press Enter:
   ```
   mysql -u your_username -p
   ```
   You'll be prompted to enter the password. Type your password and press Enter.

3. **Select the Database:**
   Once logged in, select your target database by running:
   ```sql
   USE your_database;
   ```

4. **Delete All Tables:**
   To delete all tables in the selected database, you can use the following commands:

   a. Disable foreign key checks:
   ```sql
   SET FOREIGN_KEY_CHECKS = 0;
   ```

   b. Generate and execute drop table statements:
   ```sql
   SELECT CONCAT('DROP TABLE IF EXISTS `', table_name, '`;') 
   FROM information_schema.tables 
   WHERE table_schema = 'your_database';
   ```
   Copy the output and paste it back into the MySQL prompt to execute the drop commands.

   c. Re-enable foreign key checks:
   ```sql
   SET FOREIGN_KEY_CHECKS = 1;
   ```

5. **Exit MySQL:**
   Once you've completed the steps, exit MySQL by typing:
   ```
   exit
   ```
   Then press Enter.

1. Open Command Line.

2. Log in:
   ```
   mysql -u your_username -p
   ```
   Enter your password.

3. Select database:
   ```sql
   USE your_database;
   ```

4. Disable foreign key checks:
   ```sql
   SET FOREIGN_KEY_CHECKS = 0;
   ```

5. Generate and execute drop table statements:
   ```sql
   SELECT CONCAT('DROP TABLE IF EXISTS `', table_name, '`;') 
   FROM information_schema.tables 
   WHERE table_schema = 'your_database';
   ```
   Copy and execute the output.

6. Re-enable foreign key checks:
   ```sql
   SET FOREIGN_KEY_CHECKS = 1;
   ```

7. Exit MySQL:
   ```
   exit
   ```
