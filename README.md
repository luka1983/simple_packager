Simple packager
===============

Utillity for creation of simple linux installation files. Each installation
file is assebled of one of more package units.

Purpose
-------
To create linux distro agnostic installation files by following the flow of
standard install instruction documents.


Usage
-----
Installation file creation:

1. Create package directory consisting of

		package_name/
		+-- config
		+-- script
		+-- package/

2. File _config_ should contain path to which package files located in
_package_ directory need to be extracted to. File _script_ contains bash
script that will be executed when package is istalled.

3. Run the packager script with command
		
		$ ./packager [-n installer_name] <package_dir_1> <package_dir_2> ...

4. The steps above will create <installer_name>_install.sh script.
