# Use a custom certificate

By default, Feniks Chat generates a signed certificate during the server install
process. In some cases, a server administrator may choose not to use that
feature, in which case your Feniks Chat server may be using a self-signed
certificate. This is most common for Feniks Chat servers not connected to the
public internet.

## Web

Most browsers will show a warning if you try to connect to a Feniks Chat server
with a self-signed certificate.

If you are absolutely, 100% sure that the Feniks Chat server you are connecting to
is supposed to have a self-signed certificate, click through the warnings
and follow the instructions on-screen.

If you are less than 100% sure, contact your server
administrator. Accepting a malicious self-signed certificate would
give a stranger full access to your Feniks Chat account, including your
username and password.

## Desktop

### Version 5.4.0 and above

Feniks Chat Desktop version 5.4.0 and above use the operating system's
certificate store, like your web browser.

{start_tabs}
{tab|mac}
1. Hit `Cmd` + `Space` to bring up Spotlight Search, type **Keychain
   Access**, and press Enter.

2. From the **File** menu, choose **Import Items...**

3. Navigate to the certificate file, then click **Open**.

4. Right-click the newly-added certificate, and click **Get Info** from
   the context menu.

5. Expand the **Trust** section.

6. Select **Always Trust** for the **Secure Sockets Layer (SSL)** option.

7. Close the window.  You will be prompted for your password to verify
   the change.

8. Restart the Feniks Chat Desktop application.

{tab|windows}
On Windows, Feniks Chat Desktop shares the certificate store with
Google Chrome, so you can add certificates to it from inside
Chrome.

1. Open Google Chrome.

2. From the Chrome menu (⋮) in the top-right, select **Settings**.

2. In the **Privacy and Security** section, click **Security**.

3. Scroll down to and click **Manage Certificates**.

4. Select the **Trusted Root Certification Authorities** tab.

5. Select **Import...**

6. Navigate to the certificate file, then click **Open**.

7. Select **Done**.

8. Restart the Feniks Chat Desktop application.

{tab|linux}
The required packages and steps vary by distribution; see the Chromium
documentation for [detailed documentation][linux].  On most systems,
once the `nss` tools are installed, the command to trust the
certificate is:

```
certutil -d sql:$HOME/.pki/nssdb -A -t "C,," -n Feniks Chat \
  -i path/to/certificate.pem
```

You will need to restart the Feniks Chat Desktop application to pick up the
new certificate.
{end_tabs}


### Version 5.3.0 and below

On Feniks Chat Desktop version 5.3.0 and below, we require you to manually
enter the certificate details before you can connect to your Feniks Chat
server. You'll need to get a certificate file (should end in `.crt` or
`.pem`) from your server administrator and add it:

{start_tabs}

{!desktop-sidebar-settings-menu.md!}

2. Select the **Organizations** tab.

3. Under **Add Custom Certificates**, enter your organization URL and add
   the custom certificate file (it should end in `.crt` or `.pem`).

{end_tabs}




[linux]: https://chromium.googlesource.com/chromium/src.git/+/main/docs/linux/cert_management.md
