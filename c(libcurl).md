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

[降噪接口示例]
```
CURL *hnd = curl_easy_init();

curl_easy_setopt(hnd, CURLOPT_CUSTOMREQUEST, "POST");
curl_easy_setopt(hnd, CURLOPT_URL, "http://collie.lqoptics.com/api/v1/calculate/filter/");

struct curl_slist *headers = NULL;
headers = curl_slist_append(headers, "cache-control: no-cache");
headers = curl_slist_append(headers, "Content-Type: application/json");
curl_easy_setopt(hnd, CURLOPT_HTTPHEADER, headers);


curl_easy_setopt(hnd, CURLOPT_POSTFIELDS, "{\n    \"device_sn\": \"B7BP180403\",\n    \"method\": \"classic\",\n    \"spectrum\": [\n        4832,\n        4722,\n        4683,\n        4628,\n        4665,\n        4714,\n        4711,\n        4589,\n        4292,\n        3758,\n        3758,\n        2977,\n        2153,\n        1354,\n        721,\n        277,\n        12,\n        -61,\n        -96,\n        -43,\n        17,\n        -28,\n        54,\n        184,\n        227,\n        270,\n        307,\n        324,\n        371,\n        510,\n        675,\n        852,\n        982,\n        1187,\n        1434,\n        1642,\n        1868,\n        1979,\n        2025,\n        2075,\n        1955,\n        1833,\n        1795,\n        1668,\n        1466,\n        1250,\n        1068,\n        897,\n        774,\n        719,\n        633,\n        560,\n        512,\n        536,\n        549,\n        564,\n        573,\n        476,\n        415,\n        455,\n        526,\n        838,\n        1313,\n        1876,\n        2596,\n        3442,\n        4323,\n        5199,\n        6014,\n        6706,\n        7225,\n        7512,\n        7544,\n        7388,\n        7100,\n        6716,\n        6295,\n        5892,\n        5596,\n        5416,\n        5344,\n        5462,\n        5708,\n        5978,\n        6307,\n        6564,\n        6671,\n        6670,\n        6403,\n        5915,\n        5295,\n        4597,\n        3891,\n        3235,\n        2657,\n        2177,\n        1859,\n        1716,\n        1734,\n        1890,\n        2295,\n        2877,\n        3590,\n        4460,\n        5536,\n        6652,\n        7713,\n        8709,\n        9548,\n        10267,\n        10827,\n        11139,\n        11116,\n        10812,\n        10267,\n        9512,\n        8545,\n        7468,\n        6323,\n        5149,\n        4018,\n        3012,\n        2192,\n        1605,\n        1216,\n        957,\n        798,\n        721,\n        684,\n        654,\n        653,\n        651,\n        611,\n        589,\n        575,\n        572,\n        569,\n        575,\n        602,\n        607,\n        618,\n        706,\n        822,\n        846,\n        878,\n        977,\n        953,\n        938,\n        954,\n        1023,\n        1098,\n        1152,\n        1190,\n        1231,\n        1281,\n        1315,\n        1317,\n        1266,\n        1261,\n        1272,\n        1358,\n        1407,\n        1431,\n        1392,\n        1365,\n        1335,\n        1358,\n        1566,\n        1823,\n        2117,\n        2481,\n        2949,\n        3486,\n        4053,\n        4679,\n        5189,\n        5534,\n        5722,\n        5838,\n        5798,\n        5654,\n        5331,\n        4960,\n        4605,\n        4064,\n        3504,\n        3057,\n        2671,\n        2281,\n        1973,\n        1784,\n        1716,\n        1743,\n        1804,\n        1923,\n        1873,\n        1743,\n        1619,\n        1488,\n        1317,\n        1255,\n        1266,\n        1333,\n        1375,\n        1221,\n        1105,\n        1066,\n        1066,\n        1043,\n        1074,\n        1084,\n        1057,\n        976,\n        825,\n        716,\n        645,\n        693,\n        920,\n        1382,\n        1960,\n        2835,\n        3837,\n        4811,\n        5678,\n        6362,\n        6969,\n        7408,\n        7642,\n        7673,\n        7499,\n        7095,\n        6450,\n        5639,\n        4749,\n        3876,\n        3099,\n        2391,\n        1854,\n        1579,\n        1535,\n        1823,\n        2157,\n        2599,\n        3069,\n        3464,\n        3857,\n        4139,\n        4379,\n        4482,\n        4437,\n        4301,\n        4059,\n        3697,\n        3300,\n        2889,\n        2495,\n        2112,\n        1884,\n        1695,\n        1642,\n        1608,\n        1587,\n        1671,\n        1720,\n        1702,\n        1698,\n        1656,\n        1567,\n        1416,\n        1334,\n        1247,\n        1170,\n        1075,\n        1086,\n        1191,\n        1277,\n        1396,\n        1520,\n        1579,\n        1728,\n        1798,\n        1697,\n        1656,\n        1574,\n        1605,\n        1897,\n        2422,\n        3184,\n        4331,\n        5669,\n        7067,\n        8487,\n        9700,\n        10572,\n        11164,\n        11559,\n        11905,\n        12239,\n        12640,\n        13113,\n        13635,\n        14225,\n        14930,\n        15563,\n        16205,\n        16750,\n        17080,\n        17193,\n        17164,\n        16695,\n        15812,\n        14445,\n        12588,\n        10409,\n        8218,\n        6113,\n        4307,\n        2965,\n        2104,\n        1693,\n        1730,\n        2133,\n        2722,\n        3485,\n        4252,\n        4925,\n        5461,\n        5826,\n        6064,\n        6145,\n        5978,\n        5636,\n        5201,\n        4700,\n        4118,\n        3456,\n        2878,\n        2403,\n        1984,\n        1653,\n        1471,\n        1412,\n        1424,\n        1538,\n        1604,\n        1619,\n        1567,\n        1481,\n        1418,\n        1326,\n        1180,\n        1079,\n        990]\n}");

CURLcode ret = curl_easy_perform(hnd);
```