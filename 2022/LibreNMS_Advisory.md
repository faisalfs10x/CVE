**Title:** Multiple vulnerabilities in LibreNMS <br/>
**Product:** LibreNMS <br/>
**Vulnerable Version:** prior to 22.1.0<br/>
**Fixed Version:** 22.2.0<br/>
**CVE ID:** CVE-2022-0575, CVE-2022-0576, CVE-2022-0580, CVE-2022-0587, CVE-2022-0588, CVE-2022-0589<br/>
**Homepage:** https://www.librenms.org<br/>
**Date of Discovery:** Feb 13th 2022<br/>
**Author:** Faisal Fs<br/>

---
**Vendor/product description:**

_LibreNMS is an auto-discovering PHP/MySQL/SNMP based network monitoring which includes support for a wide range of network hardware and operating systems including Cisco, Linux, FreeBSD, Juniper, Brocade, Foundry, HP and many more._

_Source: https://github.com/librenms/librenms_


**Vulnerabilities:**

1. Cross-site Scripting (XSS) - Stored in Packagist librenms/librenms 
 
    CVE-ID: CVE-2022-0575<br/>
    Risk: Medium<br/>
    Vector: CVSS:3.0/AV:N/AC:L/PR:L/UI:N/S:U/C:L/I:L/A:N<br/>
    Reference: https://github.com/advisories/GHSA-hxmr-5gv9-6p8v<br/>
    Description:<br/>
    Cross-Site Scripting vulnerability in LibreNMS v22.1.0 allows attackers to execute arbitrary javascript code in the browser of a victim which affected Devices module (Add Device) in sysName, Hardware and Community fields.


2) Cross-site Scripting (XSS) - Generic in Packagist librenms/librenms

    CVE-ID: CVE-2022-0576<br/>
    Risk: Medium<br/>
    Vector: CVSS:3.0/AV:N/AC:L/PR:L/UI:N/S:U/C:L/I:L/A:N<br/>
    Reference: https://github.com/advisories/GHSA-rp34-85x3-3764<br/>
    Description:<br/>
    Cross-Site Scripting vulnerability in LibreNMS v22.1.0 allows attackers to execute arbitrary javascript code which affected the Alerts module (Alert Transport) in the Transport name field.

3) Cross-site Scripting (XSS) - Stored in Packagist librenms/librenms

    CVE-ID: CVE-2022-0589<br/>
    Risk: Medium<br/>
    Vector: CVSS:3.0/AV:N/AC:L/PR:L/UI:N/S:U/C:L/I:N/A:L<br/>
    Reference: https://github.com/advisories/GHSA-gj26-g5qf-jrh7<br/>
    Description:<br/>
    Stored XSS in create/modify Transport Groups, Add/Edit Service and Edit Service Template.

4) Improper Access Control in Packagist librenms/librenms

    CVE-ID: CVE-2022-0580<br/>
    Risk: High<br/>
    Vector: CVSS:3.0/AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:L/A:N<br/>
    Reference: https://github.com/advisories/GHSA-33wf-4crm-2322<br/>
    Description:<br/>
    Improper Access Control vulnerability in LibreNMS v22.1.0 allows users with the normal role/level to interact with port-groups functionality such as create, edit/modify and delete the existing port group. The port-groups functionality fails to enforce policy such that normal users could act outside of their intended permissions which are supposedly accessible by the Administrator only.

5) Improper Authorization in Packagist librenms/librenms

    CVE-ID: CVE-2022-0587<br/>
    Risk: High<br/>
    Vector: CVSS:3.0/AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:L/A:N<br/>
    Reference: https://github.com/advisories/GHSA-ppfm-rj6p-38q6<br/>
    Description:<br/>
    LibreNMS v22.1.0 allows users with the normal role/level to interact with the plugin setting resulting in the users could take action such as switching on/off any installed plugins.

6) Exposure of Sensitive Information to an Unauthorized Actor in Packagist librenms/librenms

    CVE-ID: CVE-2022-0588<br/>
    Risk: High<br/>
    Vector: CVSS:3.0/AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:L/A:N<br/>
    Reference: https://github.com/advisories/GHSA-254q-rqmw-vx45<br/>
    Description:<br/>
    LibreNMS v22.1.0 allows users with the normal role/level to view/access the alert transport details. The alert transport may expose sensitive information to an actor that is not explicitly authorized to have access to that information.

**Solution:**

Update to the latest version 22.2.0


**Vendor Contact Timeline:**

2022-02-13: Contacting vendor through Discord and submitting private disclosure to huntr.dev<br/>
2022-02-13: Vendor response with acknowledgement and confirms security issue.<br/>
2022-02-16: Vendor releases security advisory through Twitter and patches is available on version 22.2.0.<br/>
2022-02-18: Public release of security advisory.
