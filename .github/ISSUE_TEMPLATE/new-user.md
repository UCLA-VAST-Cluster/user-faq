---
name: New User
about: This template is designed to be used as a checklist for a new cluster user.
title: ''
labels: 'new user'
assignees: ''

---

## Instructions

This issue is used for tracking the progress of setting you up in our cluster. Please follow the instructions below.

1. Please sign up an account on https://id.ucla-vast.com/.
2. Please fill out the required information in [Section 1](#section-1-required-information).
3. Submit this issue for review.
3. The admin will process requests. You don't have to do anything at this moment unless you have questions.
4. The admin will let you know after everything is done by replying to this issue.
5. Please follow [Section 3](#section-3-setup) and finish the checklist carefully.

## Section 1: Required Information

  + Full name:
  + Username:
  + Description of your project:
  + Your referrer (if any):

## Section 2: Process Requests

1. [ ] Forward the completed request to a faculty member or the referrer for review.
2. [ ] Grant the `cloud` access and add the user to the corresponding group.

The admin will to reply this issue after all above requests are processed.

## Section 3: Setup

1. [ ] **Mandatory** Check your account
    + Login to the jump server `cdsc0.cs.ucla.edu` via SSH
    + **Optional**
      + Setup SSH key on the jump server: `ssh-copy-id cdsc0.cs.ucla.edu`.
      + Setup SSH key for your instances: In the user settings on https://cloud.ucla-vast.com/.
    + **Optional** Setup local GUI environment
2. [ ] **Mandatory** Read the following Cluster User Guide
    + Do not install Vivado, SDAccel, or Merlin compiler in your home directory or in any of the containers. The following built-in scripts can be executed directly: `xocc`, `v++`, `vivado`, `vivado_hls`, `vitis_hls`.
    + To select the version of Vivado and Vitis (SDAccel), you can `VIV_VER=2021.1 SDA_VER=2021.1 v++`.
    + When you have I/O intensive tasks, please consider using `/tmp`.
3. [ ] **Mandatory** Create an instance on https://cloud.ucla-vast.com/
    + Please remember to increase the disk size of the instance.
    + After creating the instance, there might be several minutes of delay for initialization before you can `ssh`.  Please do not stop the instance during the initialization or you would need to recreate the instance.
    + To access your instances, you can `ssh -J cdsc0.cs.ucla.edu <one-of-the-ip-addresses>`.  For SSH config file, you can use `ProxyJump`.
    + For Windows clients, please look the instruction for tunneling.  You can also login to the jump server `cdsc0.cs.ucla.edu` first, then `ssh` from there.
    + The username and password is the same as your credentials.  If you added your SSH key in the user settings, you can access it with your key.
4. [ ] **Optional** Comment under this issue if you have any questions
5. [ ] **Mandatory** Close this issue when you are all set
