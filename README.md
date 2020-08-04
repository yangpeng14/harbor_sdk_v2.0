## Harbor Python SDK 调用方法

基于 Harbor Version 2.0+ 版本，调用 API 接口查看 Harbor 中projects、repositories、artifacts、tag等。并提供删除方法。

### 使用举例

```python
import harborclient_modify_v2_0

class GetHarborApi(object):
    def __init__(self, host, user, password, protocol="http"):
        self.host = host
        self.user = user
        self.password = password
        self.protocol = protocol
        self.client = harborclient_modify_v2_0.HarborClient(self.host, self.user, self.password, self.protocol)

    def main(self):
        print(self.client.get_projects())

if __name__ == '__main__':
    host = "harbor.example.com"
    user = "admin"
    password = "******"
    protocol = "https"
    cline_get = GetHarborApi(host, user, password, protocol)
    cline_get.main()
```
