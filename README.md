import requests
import time
url = "http://124.220.188.190:9988/api/pay.php"
#gem
payload = 'account=ID001&time=1698089873&pcid=24546&price=100&servername=1&rid=10000277&sign=b69a1bbe4bd8c149e8f508b18ab893cb'
payload1 = 'account=ID19122001&time=1698092758&pcid=24546&price=100&servername=1&rid=10000275&sign=b340f668f5f5f68271ba5e3ed8809f6a'
#goi knvs troc
payloadkn = 'account=ID001&time=1698089873&pcid=24628&price=20&servername=1&rid=10000277&sign=b69a1bbe4bd8c149e8f508b18ab893cb'
payloadkn1 = 'account=ID19122001&time=1698092758&pcid=24628&price=20&servername=1&rid=10000275&sign=b340f668f5f5f68271ba5e3ed8809f6a'
#troc tim
payloadtr = 'account=ID001&time=1698089873&pcid=24629&price=5&servername=1&rid=10000277&sign=b69a1bbe4bd8c149e8f508b18ab893cb'
payloadtr1 = 'account=ID19122001&time=1698092758&pcid=24629&price=5&servername=1&rid=10000275&sign=b340f668f5f5f68271ba5e3ed8809f6a'
headers = {
  'Content-Type': 'application/x-www-form-urlencoded'
}
while True:
  #response = requests.request("POST", url, headers=headers, data=payload)
  #response = requests.request("POST", url, headers=headers, data=payload1)

  #response = requests.request("POST", url, headers=headers, data=payloadkn)
  #response = requests.request("POST", url, headers=headers, data=payloadkn1)

  response = requests.request("POST", url, headers=headers, data=payloadtr)
  response = requests.request("POST", url, headers=headers, data=payloadtr1)
  time.sleep(5)
