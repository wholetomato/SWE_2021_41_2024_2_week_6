# SWE_2021_41_2024_2_week_6
---
## Week 4 Assignment
* https://github.com/wholetomato/SWE_2021_41_2024_02_week_4
<pre>
  <code>
    def isHappy_result(n):
    result = 0
    while n > 0:
      tmp = n%10
      n = n//10
      result += tmp ** 2
    #print(result)
    return result
  
    def in_result(result_list, n):
      result_list.append(n)
      return result_list
    
    def isHappy(n):
      result_list = []
      while n != 1:
        n = isHappy_result(n)
        if n in result_list:
          return False
        result_list = in_result(result_list, n)
      return True
  </code>
</pre>

num = 19
print(isHappy(num))

---
## Week 5 Assignment

>
>> docker exec ubuntu-container cat etc/os-release
>> * docker exec <my container> means commanding container to do something. In the upper command, I ordered "ubuntu-container" to print content in etc/os-release
>> * output
PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.1 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
>
>> docker exec ubuntu-container git --version
>> * Showing git version in the container
>> * output
git version 2.43.0
>
>> docker exec ubuntu-container python3 --version
>> * Showing python version in the container
>> * output
Python 3.12.3
>
>> docker inspect --format="{{ .HostConfig.Binds }}" ubuntu-container
>> * showing mounted directory with the container
>> * output
[ubuntu_host_dir:/mnt/ubuntu_container_dir]
