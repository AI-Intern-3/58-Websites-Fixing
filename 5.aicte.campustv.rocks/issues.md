
### Issue: Forbidden Access for https://aicte.campustv.rocks

**Steps to Resolve:**

1. **Verify File Permissions and Ensure They Are Correctly Set**

   On GoDaddy web hosting, you can typically manage file permissions via the File Manager in the GoDaddy control panel. Follow these steps:

   - **Log in to your GoDaddy account.**
   - **Navigate to your hosting dashboard.**
   - **Open the File Manager.**
   - **Locate the directory containing your website files (usually `public_html`).**
   - **Check the permissions of the files and directories.**
     - **Directories should typically be set to `755`.**
     - **Files should typically be set to `644`.**

   If permissions need adjustment:

   - **Select the directory or file in the File Manager.**
   - **Use the permissions option to set the correct values.**

   **Example:**
   - **Right-click on the directory or file, choose 'Change Permissions', and set them appropriately.**

2. **Check .htaccess Files for Restrictive Rules**

   Also managed through the File Manager:

   - **Navigate to the directory where the `.htaccess` file is located.**
   - **Open the `.htaccess` file using the File Manager’s text editor.**

   Look for restrictive rules, such as:

   ```apache
   # Example of restrictive rules
   Order Deny,Allow
   Deny from all
   ```

   - **If such rules are present, modify them to ensure they are not blocking access.**

   **Example:**
   - **Modify the `.htaccess` file to allow access if needed:**

   ```apache
   # Example of allowing all access
   Order Allow,Deny
   Allow from all
   ```

   - **Save changes and close the editor.**

**Note:** Always back up your `.htaccess` file before making changes. Ensure any modifications align with your security requirements.
```

This guide assumes you’re using GoDaddy’s File Manager for managing your files. If you have SSH access or are using FTP/SFTP, the commands and steps may differ slightly.
