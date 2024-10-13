# SWE_2021_41_2024_2_week_6
---
## Week 4 Assignment
* https://github.com/wholetomato/SWE_2021_41_2024_02_week_4
> def isHappy_result(n):
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

num = 19
print(isHappy(num))

---
## Week 5 Assignment

>
>> docker exec ubuntu-container cat etc/os-release
>> 
