# Please read this before submitting any vulnerability here

Security is a permanent process. Nothing is fully secured. 

QGIS desktop offers a programming environnement, using python and bindings. Any scripting language in desktop tools can do harm to you system. 
QGIS's plugins catalog review process forbids shipping compiled code, but we do not conduct a full security audit. It is to be considered as a free user land.  
If you are in a sensitive working environnement, please asses carefully each plugin you wish to use and deploy to your organisation. You can even create your own plugin's repository. 
Take also care to avoid any password leakage in your project files by using the secured authentication methods available, in QGIS authentication system, or on your dataproviders toolings.  

QGIS server components have been extensively tested against several type of attacks and is monitored by a dedicated continuous integration toolset. 


### Please check the issue concerns QGIS, not the packaged libraries 

QGIS.org supports two distributions (binaries) versions : 
 - Windows package via OSGEO4W project. Issues with dependencies on Windows must be raised at https://trac.osgeo.org/osgeo4w
 - Debian / Ubuntu : your OS will distribute the fixes via your update. Please get in touch with the project upstream, and use a maintained version

Other distributions 
 - Flatpak
 - Conda
 - MacOs
 - AppImage

Those distributions are maintained by the community. Maintainers will be more than thankful if you help them fix your issues by any means. 

### Please check carefully that your scanner is not raising false positives. 

We receive a lot of false positives, either from code scanner vendors mixing up client and server vulnerabilities. 

- PostgreSQL server is NOT shipped with QGIS or OSGEO. Only client libraries (libpq) and psql on Windows are. PLease double check on [PostgreSQL dedicated page](https://www.postgresql.org/support/security/) if this issue concerns the server
- Security buzz has some bad player not raisings the CVE's to upstream project are not always real or are a lot exagerated. Please read carrefully the CVE database before thinking doomsday is coming. This will save us from a lot of noise. 

### Is a QGIS issue a security issue ?

- Some crashes occur when playing with authentication system or SSL certificate. This does not mean QGIS has a vulnerability. 

### My issue concerns a plugin 

- Please contact the author of the plugin

# Reporting security issues

You think you find a real security issue in QGIS core ? 
Please report security issues and vulnerabilities to security@qgis.org
