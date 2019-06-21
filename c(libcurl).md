[消荧光接口示例]
```
CURL *hnd = curl_easy_init();
curl_easy_setopt(hnd, CURLOPT_CUSTOMREQUEST, "POST"); /*定义post请求*/
curl_easy_setopt(hnd, CURLOPT_URL, "http://collie.lqoptics.com/api/v1/calculate/fluorescence/"); /*定义接口地址*/
struct curl_slist *headers = NULL;
headers = curl_slist_append(headers, "cache-control: no-cache");
headers = curl_slist_append(headers, "Content-Type: application/json"); /*定义json类型请求*/
curl_easy_setopt(hnd, CURLOPT_HTTPHEADER, headers);

curl_easy_setopt(hnd, CURLOPT_POSTFIELDS, "{\n    \"device_sn\": \"B7BP180403\",\n    \"method\": \"fast\",\n    \"spectrum\": [\n        4832,\n        4722,\n        4683,\n        4628,\n        4665,\n        4714,\n        4711,\n        4589,\n        4292,\n        3758,\n        3758,\n        2977,\n        2153,\n        1354,\n        721,\n        277,\n        12,\n        -61,\n        -96,\n        -43,\n        17,\n        -28,\n        54,\n        184,\n        227,\n        270,\n        307,\n        324,\n        371,\n        510,\n        675,\n        852,\n        982,\n        1187,\n        1434,\n        1642,\n        1868,\n        1979,\n        2025  ]\n}");

CURLcode ret = curl_easy_perform(hnd);
```
