Here's the Markdown format for addressing various issues, including reachability, for `https://app.campusradio.rocks`, with a focus on general steps suitable for GoDaddy hosting:

```markdown
### Issue: Various Issues Including Reachability for https://app.campusradio.rocks

**Steps to Resolve:**

1. **Verify DNS Settings**

   **Check DNS Records:**

   ```bash
   # Use `dig` to check DNS records
   dig app.campusradio.rocks

   # Verify that the A record points to the correct IP address of your server
   ```

   **Check DNS Propagation:**

   - Use an online DNS propagation checker tool (e.g., [WhatsMyDNS](https://www.whatsmydns.net/)) to ensure DNS changes have propagated globally.

   **Update DNS Settings:**

   - **Log in to your GoDaddy account.**
   - **Navigate to your domain's DNS settings:**
     - **Go to your GoDaddy dashboard.**
     - **Select "My Products" and find your domain.**
     - **Click "DNS" next to the domain name.**
   - **Verify and update the A record or other relevant DNS settings if needed.**
   - **Save changes and allow time for DNS propagation.**

2. **Ensure Server is Running and Accessible**

   **Check Server Status via GoDaddy Control Panel:**

   - **Log in to your GoDaddy account.**
   - **Go to your hosting dashboard.**
   - **Check that your hosting account is active and verify the server status.**

   **Check Server Connectivity:**

   ```bash
   # Use the ping command to check if the server is reachable
   ping app.campusradio.rocks
   ```

   **Check if the Web Server Service is Running:**

   - **For shared hosting, this is managed via GoDaddy’s control panel. For other types of hosting, if you have SSH access, you might use:**
     ```bash
     # Check the status of Apache (if applicable)
     sudo systemctl status apache2
     # Check the status of Nginx (if applicable)
     sudo systemctl status nginx
     ```

   **Restart the Web Server if Necessary:**

   - **Restart the web server service through GoDaddy’s hosting control panel if there are issues.**

3. **Verify File Permissions**

   **Check and Set File Permissions:**

   - **Log in to GoDaddy’s File Manager:**
     - **Go to your GoDaddy hosting control panel.**
     - **Open the File Manager and navigate to your website’s directory.**
   - **Check the permissions of directories and files:**
     - **Directories should be set to `755`.**
     - **Files should be set to `644`.**

   **Adjust Permissions if Needed:**

   - **Select the files or directories needing permission changes.**
   - **Use the permission options in the File Manager to adjust permissions.**

**Note:** If issues persist after performing these steps, consider reaching out to GoDaddy support for further assistance. They can help with specific hosting issues that may not be resolved through general troubleshooting steps.
```

This guide provides comprehensive steps to diagnose and resolve reachability issues for your GoDaddy-hosted server, including DNS verification, server status checks, and file permissions.
