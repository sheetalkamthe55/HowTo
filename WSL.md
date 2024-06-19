Corporate network and WSL ssl/certificate problem

*Add the CA certificate(s) used by the proxy*

* Obtain the certificate(s) in Base64 encoded X.509 format.
An easy way to obtain them is through Chrome via `Settings`, `Advanced`, `Manage Certificates` on an IT managed/auto-updated system.
* Copy them to `/usr/local/share/ca-certificates`
(Optionally make a new subfolder)
* If the extension is not .crt rename the files.
* `sudo update-ca-certificates`

When repeating this exercise the certificates might not update. You can work around this by first running.

`sudo rm -f /etc/ssl/certs/[certificate-name].pem`

where `[certificate-name]` matches the filename(s) of the certificates without the original (.crt) extension.
