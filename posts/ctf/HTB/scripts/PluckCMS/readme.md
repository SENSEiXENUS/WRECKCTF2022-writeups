## CVE-2023-50564 (PoC)

This repository contains a Proof of Concept for CVE-2023-50564 vulnerability in Pluck CMS version 4.7.18

## Description

CVE-2023-50564 is a vulnerability that allows unauthorized file uploads in Pluck CMS version 4.7.18. This exploit leverages a flaw in the module installation function to upload a ZIP file containing a PHP shell, thereby enabling remote command execution.

## Usage

### Prerequisites

- Python 3.x
- The `requests` and `requests_toolbelt` packages

You can install the necessary packages with the following command:

```bash
pip install requests requests_toolbelt
```

- Usage-:

 ```bash
    ❯ ./pluckCMS.py --help
    usage: pluckCMS.py [-h] [-hst HOST] [-u USERNAME] [-p PASSWORD]
    
    options:
      -h, --help            show this help message and exit
      -hst HOST, --host HOST
                            Format: domain.com
      -u USERNAME, --username USERNAME
                            Username....
      -p PASSWORD, --password PASSWORD
                            Password....
```

- Test carried out on `greenhorn` htb lab

![image](https://github.com/user-attachments/assets/dd8bfe21-0186-4bfa-ac3a-7d5ee0aff14c)

--------------------


