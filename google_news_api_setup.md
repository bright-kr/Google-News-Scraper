## Google News API 설정하기
다음 단계에 따라 [Google News API](https://brightdata.co.kr/products/serp-api/google-search/news)를 설정합니다.
1. **Bright Data 계정에 로그인합니다.** **Web Scraper API** 탭으로 이동합니다.
2. 검색창에 **Google News**를 입력하고 선택합니다:

   <img width="650" alt="google-news-scraper-screenshot-bright-data-web-scraper-api" src="https://github.com/user-attachments/assets/53da065a-4975-4821-9ba8-9912c9da939f">

3. **Start setting an API call**을 클릭하여 API 구성을 시작합니다:

   <img width="650" alt="google-news-scraper-screenshot-start-setting-api-call" src="https://github.com/user-attachments/assets/a608922c-5f2f-46f9-b687-ed62c4eeaf97">

4. **Get API Token**을 선택하여 고유한 API 토큰을 생성합니다:

   <img width="650" alt="google-news-scraper-screenshot-get-api-token" src="https://github.com/user-attachments/assets/4e7f6044-dd26-43eb-b354-0726c87e83ce">

5. **Add token**을 클릭하여 새 토큰을 생성합니다:

   <img width="650" alt="google-news-scraper-screenshot-add-token" src="https://github.com/user-attachments/assets/f83863c7-2174-478a-9698-ed0b23e7c962">

6. API 토큰을 안전하게 저장합니다. API 호출을 수행할 때 필요합니다:

   <img width="650" alt="google-news-scraper-screenshot-new-api-token" src="https://github.com/user-attachments/assets/11d79010-94fb-41a3-9c38-3baea71aa240">

7. **Dataset ID**를 찾으려면 **Management APIs** 탭으로 이동합니다.

   <img width="650" alt="google-news-scraper-screenshot-dataset-id" src="https://github.com/user-attachments/assets/d13b7901-1c66-4a13-b3f8-71b5b2bb42ad">

8. **Data Collection APIs** 탭에서 **Add inputs**를 사용하여 여러 입력을 구성합니다:

     <img width="650" alt="google-news-scraper-screenshot-trigger-data-collection-api" src="https://github.com/user-attachments/assets/6005a9a8-430b-448e-82f2-17c390b15155">

9. 파라미터를 조정하면 오른쪽에 CURL 명령이 생성됩니다. 다음을 수행할 수 있습니다:
   - 이 명령을 사용하여 [Trigger Data Collection API](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/trigger-a-collection)를 직접 실행합니다
   - [코드](https://github.com/bright-kr/Google-News-Scraper?tab=readme-ov-file#ready-to-use-python-code)의 `_trigger_collection` 함수에 [이 파라미터를 전달](https://github.com/bright-kr/Google-News-Scraper?tab=readme-ov-file#key-input-parameters)합니다