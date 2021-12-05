<img align="right" src="https://raw.githubusercontent.com/vroncevic/gen_cc_pro/dev/docs/gen_cc_pro_logo.png" width="25%">

# Generate C++ Project

**gen_cc_pro** is shell tool for generating C++ project.

Developed in **[bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell))** code: **100%**.

[![gen_cc_pro shell checker](https://github.com/vroncevic/gen_cc_pro/workflows/gen_cc_pro%20shell%20checker/badge.svg)](https://github.com/vroncevic/gen_cc_pro/actions?query=workflow%3A%22gen_cc_pro+shell+checker%22)

The README is used to introduce the modules and provide instructions on
how to install the modules, any machine dependencies it may have and any
other information that should be provided before the modules are installed.

[![GitHub issues open](https://img.shields.io/github/issues/vroncevic/gen_cc_pro.svg)](https://github.com/vroncevic/gen_cc_pro/issues) [![GitHub contributors](https://img.shields.io/github/contributors/vroncevic/gen_cc_pro.svg)](https://github.com/vroncevic/gen_cc_pro/graphs/contributors)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Shell tool structure](#shell-tool-structure)
- [Docs](#docs)
- [Copyright and licence](#copyright-and-licence)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

### Installation

![Debian Linux OS](https://raw.githubusercontent.com/vroncevic/gen_cc_pro/dev/docs/debtux.png)

Navigate to release **[page](https://github.com/vroncevic/gen_cc_pro/releases)** download and extract release archive.

To install **gen_cc_pro** type the following

```
tar xvzf gen_cc_pro-x.y.tar.gz
cd gen_cc_pro-x.y
cp -R ~/sh_tool/bin/   /root/scripts/gen_cc_pro/ver.x.y/
cp -R ~/sh_tool/conf/  /root/scripts/gen_cc_pro/ver.x.y/
cp -R ~/sh_tool/log/   /root/scripts/gen_cc_pro/ver.x.y/
```

Self generated setup script and execution
```
./gen_cc_pro_setup.sh 

[setup] installing App/Tool/Script gen_cc_pro
	Sun 05 Dec 2021 01:49:34 PM CET
[setup] copy App/Tool/Script structure
[setup] remove github editor configuration files
[setup] set App/Tool/Script permission
[setup] create symbolic link of App/Tool/Script
[setup] done

/root/scripts/gen_cc_pro/ver.2.0/
├── bin/
│   ├── center.sh
│   ├── display_logo.sh
│   └── gen_cc_pro.sh
├── conf/
│   ├── gen_cc_pro.cfg
│   ├── gen_cc_pro.logo
│   ├── gen_cc_pro_util.cfg
│   ├── project_set.cfg
│   └── template/
│       ├── authors.template
│       ├── autogen.template
│       ├── cc_editorconfig.template
│       ├── cc_source.template
│       ├── changelog.template
│       ├── configure_ac.template
│       ├── copying.template
│       ├── makefile_am_root.template
│       ├── makefile_am_src.template
│       ├── news.template
│       └── readme.template
└── log/
    └── gen_cc_pro.log

4 directories, 19 files
lrwxrwxrwx 1 root root 50 Dec  5 13:49 /root/bin/gen_cc_pro -> /root/scripts/gen_cc_pro/ver.2.0/bin/gen_cc_pro.sh
```

Or You can use docker to create image/container.

[![gen_cc_pro docker checker](https://github.com/vroncevic/gen_cc_pro/workflows/gen_cc_pro%20docker%20checker/badge.svg)](https://github.com/vroncevic/gen_cc_pro/actions?query=workflow%3A%22gen_cc_pro+docker+checker%22)

### Usage

```
# Create symlink for shell tool
ln -s /root/scripts/gen_cc_pro/ver.x.y/bin/gen_cc_pro.sh /root/bin/gen_cc_pro

# Setting PATH
export PATH=${PATH}:/root/bin/

# Generating C++ project
gen_cc_pro rtp

gen_cc_pro ver.2.0
Sun 05 Dec 2021 01:51:23 PM CET

[check_root] Check permission for current session? [ok]
[check_root] Done

    	                                               
    	  __ _  ___ _ __     ___ ___   _ __  _ __ ___  
    	 / _` |/ _ \ '_ \   / __/ __| | '_ \| '__/ _ \ 
    	| (_| |  __/ | | | | (_| (__  | |_) | | | (_) |
    	 \__, |\___|_| |_|  \___\___| | .__/|_|  \___/ 
    	 |___/                        |_|              
    	                                               
    		Info   github.io/gen_cc_pro ver.2.0 
    		Issue  github.io/issue
    		Author vroncevic.github.io

[gen_cc_pro] Loading basic and util configuration!
100% [================================================]

[load_conf] Loading App/Tool/Script configuration!
[check_cfg] Checking configuration file [/root/scripts/gen_cc_pro/ver.2.0/conf/gen_cc_pro.cfg] [ok]
[check_cfg] Done

[load_conf] Done

[load_util_conf] Load module configuration!
[check_cfg] Checking configuration file [/root/scripts/gen_cc_pro/ver.2.0/conf/gen_cc_pro_util.cfg] [ok]
[check_cfg] Done

[load_util_conf] Done

[load_util_conf] Load module configuration!
[check_cfg] Checking configuration file [/root/scripts/gen_cc_pro/ver.2.0/conf/project_set.cfg] [ok]
[check_cfg] Done

[load_util_conf] Done

[gen_cc_pro] Generate project structure!
[gen_cc_pro] Generating directory [/data/dev/bash/3_tools/gen_cc_pro/rtp/]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/autogen.sh]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/configure.ac]
[gen_cc_pro] Generating directory [/data/dev/bash/3_tools/gen_cc_pro/rtp/po/]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/po/ChangeLog]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/po/LINGUAS]
[gen_cc_pro] Generate file [/data/dev/bash/3_tools/gen_cc_pro/rtp/po/POTFILES.in]
[gen_cc_pro] Generating directory [/data/dev/bash/3_tools/gen_cc_pro/rtp/src/]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/src/main.cc]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/src/.editorconfig]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/src/Makefile.am]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/Makefile.am]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/COPYING]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/AUTHORS]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/NEWS]
[gen_cc_pro] Generating file [/data/dev/bash/3_tools/gen_cc_pro/rtp/README]
[gen_cc_pro] Set permission!
[gen_cc_pro] Set permission!
[logging] Checking directory [/root/scripts/gen_cc_pro/ver.2.0/log/]? [ok]
[logging] Write info log!
[logging] Done

[gen_cc_pro] Done

[check_tool] Checking tool [/usr/bin/tree]? [ok]
[check_tool] Done

/data/dev/bash/3_tools/gen_cc_pro/rtp/
├── AUTHORS
├── autogen.sh
├── ChangeLog
├── configure.ac
├── COPYING
├── Makefile.am
├── NEWS
├── po
│   ├── ChangeLog
│   ├── LINGUAS
│   └── POTFILES.in
├── README
└── src
    ├── main.cc
    └── Makefile.am

2 directories, 13 files
```

### Dependencies

**gen_cc_pro** requires next modules and libraries
* sh_util [https://github.com/vroncevic/sh_util](https://github.com/vroncevic/sh_util)

### Shell tool structure

**gen_cc_pro** is based on MOP.

Shell tool structure
```
sh_tool/
├── bin/
│   ├── center.sh
│   ├── display_logo.sh
│   └── gen_cc_pro.sh
├── conf/
│   ├── gen_cc_pro.cfg
│   ├── gen_cc_pro.logo
│   ├── gen_cc_pro_util.cfg
│   ├── project_set.cfg
│   └── template/
│       ├── authors.template
│       ├── autogen.template
│       ├── cc_editorconfig.template
│       ├── cc_source.template
│       ├── changelog.template
│       ├── configure_ac.template
│       ├── copying.template
│       ├── makefile_am_root.template
│       ├── makefile_am_src.template
│       ├── news.template
│       └── readme.template
└── log/
    └── gen_cc_pro.log
```

### Docs

[![Documentation Status](https://readthedocs.org/projects/gen_cc_pro/badge/?version=latest)](https://gen_cc_pro.readthedocs.io/projects/gen_cc_pro/en/latest/?badge=latest)

More documentation and info at
* [https://gen_cc_pro.readthedocs.io/en/latest/](https://gen_cc_pro.readthedocs.io/en/latest/)
* [https://www.gnu.org/software/bash/manual/](https://www.gnu.org/software/bash/manual/)

### Copyright and licence

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Copyright (C) 2017 by [vroncevic.github.io/gen_cc_pro](https://vroncevic.github.io/gen_cc_pro)

**gen_cc_pro** is free software; you can redistribute it and/or modify
it under the same terms as Bash itself, either Bash version 4.2.47 or,
at your option, any later version of Bash 4 you may have available.

Lets help and support FSF.

[![Free Software Foundation](https://raw.githubusercontent.com/vroncevic/gen_cc_pro/dev/docs/fsf-logo_1.png)](https://my.fsf.org/)

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://my.fsf.org/donate/)
