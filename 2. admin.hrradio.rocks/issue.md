### 2. https://admin.hrradio.rocks

**Issue:** This site can't be reached

**Steps:**
1. **Verify DNS settings for hrradio.rocks:**
   - Use the `dig` command to check DNS records:
     ```sh
     dig hrradio.rocks
     dig admin.hrradio.rocks
     ```
   - Ensure A records, CNAME records, and other relevant DNS records are correctly set up.

2. **Check server status and ensure it is running:**
   - SSH into the server:
     ```sh
     ssh user@your_server_ip
     ```
   - Check the web server status (e.g., Apache or Nginx):
     ```sh
     sudo systemctl status apache2
     sudo systemctl status nginx
     ```
   - If the server is not running, start it:
     ```sh
     sudo systemctl start apache2
     sudo systemctl start nginx
     ```

3. **Review server configuration and ensure proper setup:**
   - Check the server configuration files for errors:
     - For Apache:
       ```sh
       sudo apachectl configtest
       ```
     - For Nginx:
       ```sh
       sudo nginx -t
       ```
   - Review the virtual host configuration to ensure the domain is correctly set up:
     - Apache:
       ```sh
       sudo nano /etc/apache2/sites-available/admin.hrradio.rocks.conf
       ```
     - Nginx:
       ```sh
       sudo nano /etc/nginx/sites-available/admin.hrradio.rocks
       ```
   - Restart the web server to apply any changes:
     ```sh
     sudo systemctl restart apache2
     sudo systemctl restart nginx
     ```

4. **Check firewall settings:**
   - Ensure the firewall is allowing traffic on the relevant ports (e.g., 80 for HTTP, 443 for HTTPS):
     ```sh
     sudo ufw status
     sudo ufw allow 80/tcp
     sudo ufw allow 443/tcp
     ```

5. **Check for website errors:**
   - Review the web server logs for any errors:
     - Apache:
       ```sh
       sudo tail -f /var/log/apache2/error.log
       ```
     - Nginx:
       ```sh
       sudo tail -f /var/log/nginx/error.log
       ```

6. **Verify SSL certificate:**
   - If using HTTPS, ensure the SSL certificate is valid:
     ```sh
     sudo certbot certificates
     ```
   - Renew the certificate if necessary:
     ```sh
     sudo certbot renew
     ```

Follow these steps to diagnose and fix issues with the `https://admin.hrradio.rocks` site.
