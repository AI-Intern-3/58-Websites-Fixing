
### Issue: This Site Can't Be Reached for https://aissms.collegeradio.rocks

**Steps to Resolve:**

1. **Verify DNS Settings**

   **Check DNS Records:**

   ```bash
   # Use `dig` to check DNS records
   dig aissms.collegeradio.rocks

   # Verify that the A record points to the correct IP address of your server
   ```

   **Check DNS Propagation:**

   - Use an online DNS propagation checker tool (e.g., [WhatsMyDNS](https://www.whatsmydns.net/)) to verify if DNS changes have propagated globally.

   **Update DNS Settings:**

   - **Log in to your GoDaddy account.**
   - **Navigate to your domain's DNS settings:**
     - **Go to your GoDaddy dashboard.**
     - **Select "My Products" and find your domain.**
     - **Click "DNS" next to the domain name.**
   - **Ensure that the A record is pointing to your server's IP address.**
     - **If necessary, update the A record or other relevant DNS settings.**
   - **Save changes and wait for DNS propagation.**

2. **Ensure Server is Running and Accessible**

   **Check Server Status via GoDaddy Control Panel:**

   - **Log in to your GoDaddy account.**
   - **Go to your hosting dashboard.**
   - **Ensure that your hosting account is active and the server is running.**

   **Check Server Connectivity:**

   ```bash
   # Use the ping command to check connectivity to your server
   ping aissms.collegeradio.rocks
   ```

   **Check if the Web Server Service is Running:**

   - **If you have SSH access (not common with GoDaddy's shared hosting), use these commands:**
     ```bash
     # Check the status of Apache (if applicable)
     sudo systemctl status apache2
     # Check the status of Nginx (if applicable)
     sudo systemctl status nginx
     ```

   **Restart the Web Server if Necessary:**

   - **Restart the web server service via GoDaddy’s hosting control panel if you encounter issues.**

   **Check Firewall Settings:**

   - **Ensure that firewall settings are not blocking access. This is usually managed via GoDaddy’s hosting control panel.**

**Note:** For GoDaddy web hosting, many of these tasks, such as managing DNS settings and server status, can be done through the GoDaddy control panel. If issues persist, contacting GoDaddy support for assistance is recommended.
```

This guide covers DNS verification and server accessibility specifically for GoDaddy web hosting environments.
