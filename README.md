
# Install Machine Learning Server on Windows
Smoothest process of the lot
https://docs.microsoft.com/en-us/machine-learning-server/install/machine-learning-server-windows-install


# Install Machine Learning Server on Ubuntu Linux

https://docs.microsoft.com/en-us/machine-learning-server/install/machine-learning-server-linux-install

Note that checking R is working is done using `Revo64` call, not running base R executable, like was done in Windows installation (`.\R.exe` or running the `Rgui.exe` from Windows Explorer).

Does not appear to automatically load packages like RevoScaleR into the session, but these can be loaded from `remoteLogin()` using `library()`, so they must already be installed.

If VM on Hyper-V, need to get an IP address:
https://docs.microsoft.com/en-au/windows-server/virtualization/hyper-v/Supported-Ubuntu-virtual-machines-on-Hyper-V
apt-get update
apt-get install linux-image-virtual
apt-get install linux-tools-virtual linux-cloud-tools-virtual
sudo shutdown now
Then restart

Need to enable and open ssh connection

# Install SQL Server 2017 with Machine Learing Services (In-Databse)

https://docs.microsoft.com/en-us/sql/advanced-analytics/install/sql-machine-learning-services-windows-install

Need Windows Firewall to open SQL Server port 1433
https://docs.microsoft.com/en-us/sql/sql-server/install/configure-the-windows-firewall-to-allow-sql-server-access

Need SMSS to create a server login
Easiest to download SSMS in advance and copy to VM
https://docs.microsoft.com/en-us/sql/relational-databases/security/authentication-access/create-a-login
https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms

Weird errors, sometimes R runs, sometimes not--same with Python
**R and Python worked again after reboot of entire server VM**

