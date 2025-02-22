# **Linux Command Monitoring**


## Prerequisites

- Download and install the latest version of the [Site24x7 agent](https://www.site24x7.com/app/client#/admin/inventory/add-monitor) in the server where you plan to run the plugin. 
- Download and install Python version 3 or higher.


### Plugin Installation  

- Create a directory named "LinuxCommandMonitoring"

- Download the below files and place it under the "LinuxCommandMonitoring" directory.

		wget https://raw.githubusercontent.com/site24x7/plugins/master/LinuxCommandMonitoring/LinuxCommandMonitoring.py
		wget https://raw.githubusercontent.com/site24x7/plugins/master/LinuxCommandMonitoring/LinuxCommandMonitoring.cfg


- Execute the below command to check for the valid JSON output:

		python LinuxCommandMonitoring.py --cmd=<command> --regex=<Regex> --displayname=<Display-Name>
  
- Edit the LinuxCommandMonitoring.cfg file with appropriate arguments eg:
  
		[command_1]
		cmd="grep -c ^processor /proc/cpuinfo"
		regex=None
		displayname="cpu_cores"
  
- Follow the steps in [this article](https://support.site24x7.com/portal/en/kb/articles/updating-python-path-in-a-plugin-script-for-linux-servers) to update the Python path in the LinuxCommandMonitoring.py script.

- Place the "LinuxCommandMonitoring" under the Site24x7 Linux Agent plugin directory:

        Linux    ->   /opt/site24x7/monagent/plugins/LinuxCommandMonitoring

