## Answers by Group 2

## Homework 1
	
	dpkg vs rpm

	dpkg -l ~ rpm -qa
	dpkg -l {package_name}	~ rpm -qa {package_name}
	dpkg -L {package_name}	~ rpm -ql {package_name}
	dpkg -i {package_name}	~ rpm -i {package_name}
	dpkg -r {package_name}	~ rpm -e {package_name}
	dpkg -P {package_name}  ~ rpm -e {package_name}									
	dpkg -c {package_name}	~ rpm -qpl {package_name}
	dpkg -S {/path/to/file}	~ rpm -qf {/path/to/file}
	dpkg -p {package_name}  ~
	dpkg -s {package_name}  ~ rpm -qi {package_name}
	dpkg --get-selections	~


	apt vs yum

	apt policy
	add-apt repository {repository_name}
	apt list ~	yum list
	apt install {package_name}  ~ yum install {package_name}
	apt search {package_name}  ~	yum search {package_name}
	apt update  ~  yum update
	apt upgrade
	apt remove {package_name}  ~  yum remove {package_name}
	apt purge {package_name}										
	apt autoremove


## Homework 2

```
	- sudo apt install alien
	- sudo alien bless-0.6.0-2
	- sudo dpkg -i bless-0.6.0-22_amd64.deb
```

## Homework 3

```
	function take_last_modified() {
		ls -1t | head -5
	}

	alias last_modified=take_last_modified

```

## Homework 4

```
	function get_code_name() {
		grep "CODENAME" /etc/lsb-release | awk -F "=" '{print $2}'
	}
	PS1="{$(get_code_name)}\u@\h:\w\$"

```

## Homework 5

```
	alias kill_all_process='kill  $(ps aux | grep $1 | awk '{print $2}')'
```

## Homework 6

```
	function get_branch() {
		git branch | '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
	}

	alias gplo='git pull origin $get_branch'
```
