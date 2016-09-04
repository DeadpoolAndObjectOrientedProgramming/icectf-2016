# IceCTF 2016 : Complacent

**Category:** Reconnaissance
**Points:** 40
**Solves:** 1009
**Description:**

These silly bankers have gotten pretty complacent with their self signed SSL certificate. I wonder if there's anything in there. [complacent.vuln.icec.tf](https://complacent.vuln.icec.tf/)

## Write-up

The description pointed me to the SSL certificate but I couldn't view all the info for it in my browser so I googled for this solution that gave me the following command:

```
openssl s_client -connect complacent.vuln.icec.tf:443 -showcerts
```

and in the certificate digest was the flag. The flag was as part of the Organization Unit. 

You can also see the flag looking at the cert in the browser:

![cert](https://cloud.githubusercontent.com/assets/3537289/18232109/7fb305a0-72b8-11e6-9bb8-f7b5515e0b37.png)

See [#11](https://github.com/ikornaselur/project-firewater/issues/11)
