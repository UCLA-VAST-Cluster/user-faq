---
name: New User
about: This template is designed to be used as a checklist for a new cluster user.
title: ''
labels: 'new user'
assignees: ''

---

## Instructions

This issue is used for tracking the progress of setting you up in our cluster. Please follow the instructions below.

1. Please fill out the required information in [Section 1](#section-1-required-information).
2. Submit this issue so that the admins can see.
3. The admin will process requests in [Section 2](#section-2-process-requests-for-admin). You don't have to do anything at this moment unless you have questions.
4. The admin will let you know after everything is done by replying to this issue.
5. Please follow [Section 3](#section-3-setup) and finish the checklist carefully.

## Section 1: Required Information

**1. Information for applying a NIS account.**
  + Full name:
  + Preferred username:
  + Permanent email:
  

*Check https://vast.cs.ucla.edu/cluster/ to see which server is generally idle before applying.*
  
**2. Information for applying a container.**
  + How many server nodes do you need?
    + `n0`\~`n7` and `n10`\~`n21` available, some of them might be down temporarily
    + `n1` and `n21` might be rebooted without notice due to potential FPGA stuck
  + For each node, do you want a *CentOS 7*, *Ubuntu 16.04*, or *Ubuntu 18.04* container?
    + Ubuntu is generally friendlier to use and better supported by most software
  + **Optional** Which packages would you like to be pre-installed in each container?
    + We will execute `apt install <packages>` or `yum install <packages>` before creating the containers
    + Only packages from the official repo can be pre-installed; if not sure, search https://pkgs.org/
  
## Section 2: Process Requests (for admin)

1. [ ] Create a NIS account and update GitHub mapping
2. [ ] Create the container(s)

The admin will to reply this issue after all above requests are processed.

## Section 3: Setup

1. [ ] **Mandatory** Check your NIS account
    + You will receive your temporary password via the email you provided.
    + Login to `cdsc0.cs.ucla.edu`, run `yppasswd`, and **CHANGE YOUR PASSWORD**
    + **Optional** Setup SSH key
    + **Optional** Setup local GUI environment
2. [ ] **Optional** Comment under this issue if you have any questions
3. [ ] **Mandatory** Close this issue when you are all set
