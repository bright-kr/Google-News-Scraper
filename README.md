# Google News Scraper

[![Promo](https://github.com/bright-kr/Google-News-Scraper/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.co.kr/products/serp-api/google-search/news?promo=github15) 

이 리포지토리는 Google News에서 뉴스 데이터를 수집하는 두 가지 방법을 제공합니다.
- **무료 방법:** 소규모 프로젝트 및 학습에 적합합니다
- **Google News API:** 대규모의 신뢰할 수 있는 실시간 데이터 추출에 이상적입니다

## Table of Contents

- [Method 1: Free Google News Scraper](#method-1-free-google-news-scraper)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Output](#output)
- [Common Scraping Challenges](#common-scraping-challenges)
- [Method 2: Bright Data Google News API](#method-2-bright-data-google-news-api)
  - [Key Benefits](#key-benefits)
  - [Getting Started with the Google News API](#getting-started-with-the-google-news-api)
  - [Key Input Parameters](#key-input-parameters)
  - [Sample Result](#sample-result)
  - [Ready-to-Use Python Code](#ready-to-use-python-code)
  - [Understanding the API Implementation](#understanding-the-api-implementation)
  - [Customizing Your Data Collection](#customizing-your-data-collection)

## Method 1: Free Google News Scraper
<img width="700" alt="image" src="https://github.com/user-attachments/assets/a7d34ffe-17c6-4c59-acbf-aaf84ed1b13e">

이 무료 도구를 사용하면 관심 있는 어떤 주제든 기반으로 뉴스 기사를 수집할 수 있습니다. 헤드라인부터 발행 날짜까지 모든 정보를 깔끔하게 정리된 형태로 받을 수 있습니다.

### Prerequisites
- Python 3.9+
- 두 가지 주요 패키지:
  - [aiohttp](https://pypi.org/project/aiohttp/) (リクエスト를 보내기 위해 사용합니다)
  - [beautifulsoup4](https://pypi.org/project/beautifulsoup4/) (HTML을 파싱하기 위해 사용합니다)

### Installation
1. 리포지토리를 클론합니다:

    ```bash
    git clone https://github.com/bright-kr/Google-News-Scraper.git
    ```
3. 프로젝트 디렉터리로 이동합니다:

    ```bash
    cd Google-News-Scraper
    ```
4. 필요한 의존성을 설치합니다:

    ```bash
    pip install -r requirements.txt
    ```
### Usage
1. `free_scraper` 디렉터리로 이동한 다음 `main.py`를 엽니다
2. 파일에서 검색어를 정의합니다:

    ```bash
    search_terms = [
        "artificial intelligence",
        "climate change",
        "space exploration",
        # Add more search terms as needed
    ]
    ```
3. スクレイパー를 실행합니다:

    ```bash
    python main.py
    ```
### Output
スクレイパー는 JSON 파일을 생성합니다:
- 각 검색어별 개별 JSON 파일
- 모든 검색어의 데이터를 포함하는 `combined_results.json` 파일

JSON 출력에서 각 기사는 다음을 포함합니다:
```json
{
    "title": "OpenAI launches full o1 model with image uploads and analysis, debuts ChatGPT Pro - VentureBeat",
    "link": "https://news.google.com/rss/articles/CBMipgFBVV95cUxQTTVmS1I4aW1QanZXTnBfa2tBR3d0Y2JzNjJJNldBZTd1TVVfRmpxaUM3bGJld3RycXhPbU8wM1loT0JGd2JDRzFmU1pLU3FSbkRRZ0FPY29INmdhU1RsWXFqXzdLTjNCbU5ES3pIQXZLbTVmMWVhc0FqVlljeWNPOHZMeFlXV2F5Q21ac0lSZVhIOHlnS05sdkR5ZjhJTU9HazJ6MWJR?oc=5",
    "publication_date": "Thu, 05 Dec 2024 18:00:00 GMT",
    "source": "VentureBeat",
    "source_url": "https://venturebeat.com",
    "guid": "CBMipgFBVV95cUxQTTVmS1I4aW1QanZXTnBfa2tBR3d0Y2JzNjJJNldBZTd1TVVfRmpxaUM3bGJld3RycXhPbU8wM1loT0JGd2JDRzFmU1pLU3FSbkRRZ0FPY29INmdhU1RsWXFqXzdLTjNCbU5ES3pIQXZLbTVmMWVhc0FqVlljeWNPOHZMeFlXV2F5Q21ac0lSZVhIOHlnS05sdkR5ZjhJTU9HazJ6MWJR",
}
```

👉 전체 예시 출력은 [free_scraper/data/](https://github.com/bright-kr/Google-News-Scraper/tree/main/free_scraper/data) 디렉터리에서 확인할 수 있습니다.

## Common Scraping Challenges
Google News에서 데이터를 スクレイピング하는 것은 꽤 까다로울 수 있습니다. 다음은 흔히 마주칠 수 있는 이슈들입니다:
1. **CAPTCHA 및 アンチボット 메커니즘:** Google은 봇이 콘텐츠에 접근하는 것을 막기 위해 CAPTCHA 또는 レート制限 메커니즘을 자주 사용합니다.
2. **확장성:** 대량의 데이터를 スクレイピング하거나 고빈도 スクレイピング을 수행하면 무료 スクレイパー가 과부하될 수 있습니다.
3. **글로벌 및 로컬라이즈드 뉴스 접근:** 서로 다른 지역과 언어에 맞게 スクレイパー를 커스터마이징하려면 상당한 노력과 수동 조정이 필요한 경우가 많습니다.

## Method 2: Bright Data Google News API
더 강력한 솔루션을 원하시나요? [Bright Data's Google News API](https://brightdata.co.kr/products/serp-api/google-search/news)에 대해 알아보겠습니다. 고려할 만한 이유는 다음과 같습니다:

### Key Benefits
- **인프라 걱정 제로:** プロキシ 및 CAPTCHA를 신경 쓸 필요가 없습니다
- **확장성에 최적화:** 뛰어난 성능으로 높은 트래픽을 처리합니다
- **글로벌 범위:** 어느 국가에서든, 어떤 언어로든 뉴스를 가져올 수 있습니다
- **프라이버시 우선:** GDPR 및 CCPA 준수
- **성공 기반 과금:** 성공한 リクエスト에 대해서만 과금됩니다
- **구매 전 테스트:** 테스트를 위한 무료 API 호출 20회 제공

## Getting Started with the Google News API
> Google News API 설정에 대한 자세한 가이드는 [Step-by-Step Setup Guide](https://github.com/bright-kr/Google-News-Scraper/blob/main/google_news_api_setup.md)를 확인하십시오.
### Key Input Parameters
| **Parameter**| **Required?** | **Description**                                            | **Example**               |
|---------------|--------------|------------------------------------------------------------|---------------------------|
| `url`         | Yes          | 기본 Google News URL                                   | `news.google.com`|
| `keyword`     | Yes          | 검색 주제                        | `"ChatGPT"`             |
| `country`     | No           | 뉴스를 가져올 국가                                | `"US"`                    |
| `language`    | No           | 원하는 언어                                | `"en"`                    |

### Sample Result
API는 다음과 같은 결과를 반환합니다:
```json
{
    "url": "https://www.tomsguide.com/news/live/12-days-of-openai-live-blog-chatgpt-sora",
    "title": "12 Days of OpenAI Day 2 LIVE: o1 full is here and every new ChatGPT AI announcement as it happens",
    "publisher": "Tom's Guide",
    "date": "2024-12-06T20:54:01.000Z",
    "category": null,
    "keyword": "chatgpt",
    "country": "US",
    "image": "https://news.google.com/api/attachments/CC8iK0NnNW9SbTFVTWtkNGFGSjJSVGhGVFJDb0FSaXNBaWdCTWdhQmtJcWpOQWM=-w200-h112-p-df-rw",
    "timestamp": "2024-12-08T10:06:05.122Z",
    "input": {
        "url": "https://news.google.com/",
        "keyword": "chatgpt",
        "country": "US",
        "language": "en",
    },
}
```
👉 전체 예시 출력은 [news_scraper_output.json](https://github.com/bright-kr/Google-News-Scraper/blob/main/google-news-api-scraper/data/news_scraper_output.json) 파일에서 확인할 수 있습니다.

### Ready-to-Use Python Code
다음은 시작을 위한 스크립트입니다:
```python
import requests
import json
import time


class BrightDataNews:
    def __init__(self, api_token):
        self.api_token = api_token
        self.headers = {
            "Authorization": f"Bearer {api_token}",
            "Content-Type": "application/json",
        }
        self.dataset_id = "gd_lnsxoxzi1omrwnka5r"

    def collect_news(self, search_queries):
        """
        Collect Google News articles using BrightData API
        """
        # 1. Trigger data collection
        print("Starting news collection...")
        trigger_response = self._trigger_collection(search_queries)
        snapshot_id = trigger_response.get("snapshot_id")
        print(f"Snapshot ID: {snapshot_id}")

        # 2. Wait for data to be ready
        print("Waiting for data...")
        while True:
            status = self._check_status(snapshot_id)
            print(f"Status: {status}")

            if status == "ready":
                # Check if data is actually available
                data = self._get_data(snapshot_id)
                if data and len(data) > 0:
                    break
            time.sleep(10)  # Wait 10 seconds before next check
        # 3. Get and save the data
        print("Saving data...")
        filename = f"news_scraper_output.json"
        with open(filename, "w", encoding="utf-8") as f:
            json.dump(data, f, indent=2, ensure_ascii=False)
        print(f"✓ Data saved to {filename}")
        print(f"✓ Collected {len(data)} news articles")
        return data

    def _trigger_collection(self, search_queries):
        """Trigger news data collection"""
        response = requests.post(
            "https://api.brightdata.com/datasets/v3/trigger",
            headers=self.headers,
            params={"dataset_id": self.dataset_id, "include_errors": "true"},
            json=search_queries,
        )
        return response.json()

    def _check_status(self, snapshot_id):
        """Check collection status"""
        response = requests.get(
            f"https://api.brightdata.com/datasets/v3/progress/{snapshot_id}",
            headers=self.headers,
        )
        return response.json().get("status")

    def _get_data(self, snapshot_id):
        """Get collected data"""
        response = requests.get(
            f"https://api.brightdata.com/datasets/v3/snapshot/{snapshot_id}",
            headers=self.headers,
            params={"format": "json"},
        )
        return response.json()
```
사용 방법은 다음과 같습니다:
```python
# Initialize the client
news_client = BrightDataNews("<YOUR_API_TOKEN>")

# Define what you want to collect
queries = [
    {
        "url": "https://news.google.com/",
        "keyword": "artificial intelligence startups",
        "country": "US",
        "language": "en",
    },
    {
        "url": "https://news.google.com/",
        "keyword": "tech industry layoffs",
        "country": "US",
        "language": "en",
    },
]

# Start collection
try:
    news_data = news_client.collect_news(queries)
    print(f"Successfully collected {len(news_data)} articles")
except Exception as e:
    print(f"Collection failed: {str(e)}")
```
### Understanding the API Implementation
1. **API 토큰 설정**
    - 우선 API 토큰이 필요합니다
    - 아직 토큰이 없다면 [setup guide](https://github.com/bright-kr/Google-News-Scraper/blob/main/google_news_api_setup.md)를 확인하십시오
2. **수집 시작**
    - 검색 파라미터를 API에 전달합니다
    - 그러면 `snapshot_id`가 반환됩니다
3. **진행 상황 모니터링**
    - 이 프로세스는 몇 분 정도 걸립니다
    - 본 코드는 상태를 자동으로 확인합니다:
      - "running" = 데이터 수집이 아직 진행 중입니다
      - "ready" = 결과를 수집할 시간입니다!
4. **데이터 가져오기**
    - 상태가 "ready"로 표시되면 결과를 가져와 저장합니다
    - 데이터는 정돈된 JSON 형식으로 제공됩니다
    - 각 기사에는 앞서 설명한 모든 필드가 포함됩니다

## Customizing Your Data Collection
다음 파라미터를 사용하여 결과를 세밀하게 조정할 수 있습니다:
| **Parameter**       | **Type**   | **Description**                                            | **Example**                  |
|---------------------|------------|------------------------------------------------------------|------------------------------|
| `limit`             | `integer`  | 입력당 최대 결과 수                                   | `limit=10`                   |
| `include_errors`    | `boolean`  | 트러블슈팅을 위한 오류 보고서를 가져옵니다                     | `include_errors=true`        |
| `notify`            | `url`      | 완료 시 알림을 받을 Webhook 알림 URL  | `notify=https://notify-me.com/` |
| `format`            | `enum`     | 출력 형식(예: JSON, NDJSON, JSONL, CSV)         | `format=json`                |

💡 **Pro Tip:** 데이터를 [external storage](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/overview#via-deliver-to-external-storage)로 전달할지, 또는 [webhook](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/overview#via-webhook)으로 전달할지도 선택할 수 있습니다.

----

더 많은 세부 정보가 필요하신가요? [official API docs](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/overview)를 확인하십시오.