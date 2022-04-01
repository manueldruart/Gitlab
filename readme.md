# Gitlab 
<img src="https://gitlab.com/">

# Prerequisites
* Have a gitlab server or an account on gitlab.com

# Install Gitlab-runner
* Add the official Gitlab repository
  For Debian/Ubuntu/Mint:
  ```
  curl -L "https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh" | sudo bash

  ```
  For RHEL/CentOS/Fedora: 
    ```
  curl -L "https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.rpm.sh" | sudo bash

  ```

  * Install the latest version of GitLab Runner

  ```
  sudo apt-get install gitlab-runner


  ```
  For RHEL/CentOS/Fedora: 
    ```
  sudo yum install gitlab-runner


  ```

  # Install a runner in your project
  In your Gitlab prohect go to Settings > CI/CD > Runners > Expand
  In this case we will use a specific runners.
  On your machine hosting the gitlab runner apply these commands:
  ```
  sudo curl -L --output /usr/local/bin/gitlab-runner https://gitlab-runner-downloads.s3.amazonaws.com/latest/binaries/gitlab-runner-linux-amd64

  ```
  ```
  sudo chmod +x /usr/local/bin/gitlab-runner
  ```
  ```
  sudo gitlab-runner register --url https://gitlab.com/ --registration-token $REGISTRATION_TOKEN
  ```

  disable shared runners
  
  Refresh your gitlab page 

  