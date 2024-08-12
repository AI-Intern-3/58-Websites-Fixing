Here's the Markdown format with solutions for addressing various issues, including reachability, for `https://app.campusradio.rocks`:

```markdown
### Issue: Various Issues Including Reachability for https://app.campusradio.rocks

**Steps to Resolve:**

1. **Verify DNS Settings**

   **Check DNS Records:**

   ```bash
   # Use `dig` to check DNS records for the domain
   dig app.campusradio.rocks

   # Example output should show the IP address that the domain resolves to
   ```

   **Check DNS Propagation:**

   - Use an online DNS propagation checker tool to verify global propagation:
     - Visit [WhatsMyDNS](https://www.whatsmydns.net/) or a similar DNS propagation checker.
     - Enter `app.campusradio.rocks` and review the results.

   **Update DNS Settings:**

   - **Log in to your GoDaddy account.**
   - **Navigate to your domain's DNS settings:**
     - **Go to your GoDaddy dashboard.**
     - **Select "My Products" and locate your domain.**
     - **Click "DNS" next to the domain name.**
   - **Ensure that the DNS records (especially A records) are correctly configured to point to the correct IP address of your server.**
   - **Update DNS records if necessary and save changes.**
   - **Allow time for DNS propagation, which may take up to 48 hours.**

2. **Ensure Server is Running and Accessible**

   **Check Server Status via GoDaddy Control Panel:**

   - **Log in to your GoDaddy account.**
   - **Navigate to your hosting dashboard.**
   - **Verify that your hosting account is active and that the server is running.**

   **Check Server Connectivity:**

   ```bash
   # Use the ping command to check if the server is reachable
   ping app.campusradio.rocks
   ```

   **Check if the Web Server Service is Running:**

   - **For GoDaddy's shared hosting, use the hosting control panel to check the status.**
   - **If you have SSH access, you might use:**
     ```bash
     # Check the status of Apache (if applicable)
     sudo systemctl status apache2
     # Check the status of Nginx (if applicable)
     sudo systemctl status nginx
     ```

   **Restart the Web Server if Necessary:**

   - **Restart the web server service through GoDaddy’s hosting control panel if there are issues.**

3. **Verify File Permissions**

   **Check and Adjust File Permissions via GoDaddy File Manager:**

   - **Log in to your GoDaddy account.**
   - **Go to your hosting control panel and open the File Manager.**
   - **Navigate to the directory containing your website files (typically `public_html`).**
   - **Check and adjust permissions:**
     - **Directories should generally be set to `755`.**
     - **Files should generally be set to `644`.**
   - **Modify permissions as needed using the File Manager’s permission settings.**

**Note:** For persistent issues after following these steps, contacting GoDaddy support for assistance may be necessary, especially if the problem is related to specific hosting configurations or issues beyond general troubleshooting.
```

This guide provides a comprehensive approach to troubleshooting various issues, including reachability, for a GoDaddy-hosted server.
