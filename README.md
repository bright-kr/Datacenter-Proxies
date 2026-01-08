# Bright Data データセンタープロキシ

[![Promo](https://github.com/bright-kr/Datacenter-Proxies/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.co.kr/proxy-types/datacenter-proxies?promo=github15)

## Overview
신뢰할 수 있는 데이터 수집과 Webスクレイピング을 위해, 탁월한 규모와 속도를 갖춘 Bright Data의 광범위한 [データセンタープロキシ network](https://brightdata.co.kr/proxy-types/datacenter-proxies)을 활용하십시오.

- **770,000+ データセンター IPs**
- **[Shared](https://brightdata.co.kr/solutions/shared-proxies) 및 [Dedicated](https://brightdata.co.kr/solutions/dedicated-proxies) IP 옵션**
- **~0.24s 평균 レスポンス 시간**
- **HTTP(S) 및 [SOCKS5](https://brightdata.co.kr/solutions/socks5-proxies) 지원**
- **무료 국가 단위 타기팅**

## Key Features
- **Global Reach**: [98개 국가](https://brightdata.co.kr/locations)에 걸친 データセンター IPs에 액세스합니다.
- **High Success Rates**: スクレイピング 작업에서 최대 99.9%의 성공률을 달성합니다.
- **Fast and Reliable**: 99.99% 네트워크 가동 시간과 빠른 연결 속도를 제공합니다.
- **Customizable Options**: 필요에 따라 shared 또는 dedicated IPs 중에서 선택합니다.
- **Unlimited Scaling**: 제한 없이 동시 セッション을 지원합니다.

## Pricing Plans
- **Pay As You Go**: 월 약정 없이 $0.6/GB로 이용할 수 있습니다.
- **Monthly Subscriptions - Shared**:
  - **10 IPs**: $1.40/IP, $14/month + VAT.
  - **100 IPs**: $1.00/IP, $100/month + VAT.
  - **500 IPs**: $0.95/IP, $475/month + VAT.
  - **1,000 IPs**: $0.90/IP, $900/month + VAT.
  - **Enterprise Plans**: 대규모 데이터 수집을 위한 맞춤형 솔루션입니다.

- **Monthly Subscriptions - Dedicated**:
  - **10 IPs**: $2.20/IP, $22/month + VAT.
  - **100 IPs**: $1.70/IP, $170/month + VAT.
  - **500 IPs**: $1.50/IP, $750/month + VAT.
  - **1,000 IPs**: $1.30/IP, $1300/month + VAT.
  - **Enterprise Plans**: 대규모 데이터 수집을 위한 맞춤형 솔루션입니다.


- **Monthly Subscriptions - Pay/GB**:
  - $0.51/GB, $499/month + VAT.
  - $0.45/GB, $999/month + VAT.
  - $0.42/GB, $1999/month + VAT.
  - **Enterprise Plans**: 대규모 데이터 수집을 위한 맞춤형 솔루션입니다.

가입하고 첫 입금에 대해 최대 $500까지 1달러당 1달러 매칭 혜택을 받으십시오!

## Getting Started with Datacenter Proxies
1. **Start Free Trial**: 신용카드 없이 시작할 수 있습니다.
2. **Integration**: API 또는 Bright Data Control Panel을 통해 IPs 및 구성을 관리합니다.
3. **Supported Languages**: Python, Java, C#, Node.js 및 Shell용 빠른 시작 가이드가 제공됩니다.

## Code Examples

### Python

```python
import sys

# Replace '[your customerID]', 'datacenter', and '[your password]' with your actual Bright Data customer ID, zone, and password
if sys.version_info[0] == 2:
    import six
    from six.moves.urllib import request
    opener = request.build_opener(
        request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())

if sys.version_info[0] == 3:
    import urllib.request
    opener = urllib.request.build_opener(
        urllib.request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())
```

### Java

```java
package example;

import org.apache.http.HttpHost;
import org.apache.http.client.fluent.*;

public class Example {
    public static void main(String[] args) throws Exception {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        HttpHost proxy = new HttpHost("brd.superproxy.io", 22225);
        String res = Executor.newInstance()
            .auth(proxy, "brd-customer-[your customerID]-zone-datacenter", "[your password]")
            .execute(Request.Get("https://geo.brdtest.com/mygeo.json").viaProxy(proxy))
            .returnContent().asString();
        System.out.println(res);
    }
}
```

### C#

```c#
using System;
using System.Net;

class Example
{
    static void Main()
    {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        var client = new WebClient();
        client.Proxy = new WebProxy("brd.superproxy.io:22225");
        client.Proxy.Credentials = new NetworkCredential("brd-customer-[your customerID]-zone-datacenter", "[your password]");
        Console.WriteLine(client.DownloadString("https://geo.brdtest.com/mygeo.json"));
    }
}
```

### Node.js

```node.js
require('request-promise')({
    url: 'https://geo.brdtest.com/mygeo.json',
    proxy: 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225',
    })
.then(function(data){ console.log(data); },
    function(err){ console.error(err); });
```

### Shell

```shell
# Replace '[your customerID]' and '[your password]' with your actual credentials
curl --proxy brd.superproxy.io:22225 --proxy-user brd-customer-[your customerID]-zone-residential:[your password] -k "https://geo.brdtest.com/mygeo.json"
```

## Integrations
당사의 データセンタープロキシ는 다음을 포함한 인기 자동화 도구와 호환됩니다:

- [**Puppeteer**](https://brightdata.co.kr/integration/puppeteer)
- [**Selenium**](https://brightdata.co.kr/integration/selenium)
- [**Playwright**](https://brightdata.co.kr/integration/playwright)
- [**AdsPower**](https://brightdata.co.kr/integration/adspower)
- [**MultiLogin**](https://brightdata.co.kr/integration/multilogin)

## Use Cases
データセンタープロキシ의 일반적인 활용 사례는 다음과 같습니다:

- [**eCommerce**](https://brightdata.co.kr/use-cases/ecommerce): 가격 및 제품 재고 여부를 추적합니다.
- [**Social Media**](https://brightdata.co.kr/use-cases/social-media-for-marketing): 트렌드 및 참여도를 모니터링합니다.
- [**Real Estate**](https://brightdata.co.kr/use-cases/real-estate): 부동산 매물 데이터 수집을 수행합니다.
- [**Travel**](https://brightdata.co.kr/use-cases/travel): 지역별 여행 상품을 비교합니다.

## FAQ

### What is a Datacenter Proxy?
データセンタープロキシ는 서버에 할당된 IPs를 제공하여, Webスクレイピング 및 기타 사용 사례를 위해 IPアドレス와 위치를 변경할 수 있도록 합니다.

### What are the advantages of Datacenter Proxies?
データセンタープロキシ는 빠르고 비용 효율적이며, 간단한 데이터 수집 작업, 계정 관리, 기본적인 지리적 제한 우회에 이상적입니다.

### How are Datacenter Proxies used by businesses?
경쟁 분석부터 디지털 자산 보호까지, データセンタープロキシ는 다양한 산업 전반에서 폭넓은 작업을 지원합니다.

### Where are Bright Data's Datacenter Proxies located?
당사의 プロキシ는 전 세계 98개 지오ロ케ーション에 걸쳐 있으며, [USA](https://brightdata.co.kr/locations/united-states), [Canada](https://brightdata.co.kr/locations/ca), [UK](https://brightdata.co.kr/locations/gb), [Germany](https://brightdata.co.kr/locations/de), [France](https://brightdata.co.kr/locations/fr)에서 높은 IP 수를 제공합니다.

### Are Datacenter Proxies fast?
예, 최소한의 라우팅으로 データセンタープロキシ는 빠른 연결을 제공하므로, 시간 민감형 애플리케이션에 최적입니다.

### Should I use shared or dedicated Datacenter Proxies?
독점적 사용이 필요하면 dedicated プロキシ를 사용하시고, 일반적인 スクレイピング 및 테스트 작업을 비용 효율적으로 수행하려면 shared プロキシ를 사용하십시오.