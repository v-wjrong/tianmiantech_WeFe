# Basic Information

|      |      |
|------|------|
| Name | HttpRequest |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/http/HttpRequest.java |
| Package Name | com.welab.wefe.common.http |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.common.util.UrlUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.apache.http.HttpEntity', 'org.apache.http.NameValuePair', 'org.apache.http.client.config.RequestConfig', 'org.apache.http.client.entity.UrlEncodedFormEntity', 'org.apache.http.client.methods.CloseableHttpResponse', 'org.apache.http.client.methods.HttpGet', 'org.apache.http.client.methods.HttpPost', 'org.apache.http.client.methods.HttpUriRequest', 'org.apache.http.config.Registry', 'org.apache.http.config.RegistryBuilder', 'org.apache.http.conn.socket.ConnectionSocketFactory', 'org.apache.http.conn.socket.PlainConnectionSocketFactory', 'org.apache.http.conn.ssl.NoopHostnameVerifier', 'org.apache.http.conn.ssl.SSLConnectionSocketFactory', 'org.apache.http.entity.ContentType', 'org.apache.http.entity.StringEntity', 'org.apache.http.entity.mime.MultipartEntityBuilder', 'org.apache.http.entity.mime.content.InputStreamBody', 'org.apache.http.impl.client.BasicCookieStore', 'org.apache.http.impl.client.CloseableHttpClient', 'org.apache.http.impl.client.HttpClients', 'org.apache.http.impl.conn.PoolingHttpClientConnectionManager', 'org.apache.http.message.BasicNameValuePair', 'org.apache.http.ssl.SSLContextBuilder', 'org.apache.http.util.EntityUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'javax.net.ssl.SSLContext', 'java.io.File', 'java.io.InputStream', 'java.io.UnsupportedEncodingException', 'java.nio.charset.Charset', 'java.nio.charset.StandardCharsets', 'java.security.KeyManagementException', 'java.security.KeyStoreException', 'java.security.NoSuchAlgorithmException', 'java.util', 'java.util.function.Function'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HttpRequest | class |  |



## Class HttpRequest

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | HttpRequest |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| connectTimeout = 10 * 1000 | int |  |
| url | String |  |
| cookieStore = new BasicCookieStore() | BasicCookieStore |  |
| needPrintLog = true | boolean |  |
| LOG = LoggerFactory.getLogger(HttpRequest.class) | Logger |  |
| encoding = StandardCharsets.UTF_8.name() | String |  |
| RETRY_DELAY_STEP = 300 | long |  |
| validator | Function<HttpResponse, Boolean> |  |
| sConnectionManager = null | PoolingHttpClientConnectionManager |  |
| USER_AGENT = "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_12_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/63.0.3239.132 Safari/537.36" | String |  |
| paramMap = new HashMap<>() | Map<String, Object> |  |
| socketTimeout = 10 * 1000 | int |  |
| retryDelay = 0 | long |  |
| contentType | String |  |
| sessionId = UUID.randomUUID().toString().replace("-", "") | String |  |
| body | String |  |
| headers | Map<String, String> |  |
| retryCount = 1 | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setBody | HttpRequest |  |
| getBody | String |  |
| closeLog | HttpRequest |  |
| get | HttpResponse |  |
| create | HttpRequest |  |
| getParamMap | Map<String, Object> |  |
| setRetryCount | HttpRequest |  |
| post | HttpResponse |  |
| setValidator | HttpRequest |  |
| doHttp | HttpResponse |  |
| setCookieStore | HttpRequest |  |
| postJson | HttpResponse |  |
| appendParameter | HttpRequest |  |
| setConnectTimeout | HttpRequest |  |
| setEncoding | HttpRequest |  |
| setSocketTimeout | HttpRequest |  |
| appendParameters | HttpRequest |  |
| putHeaders | HttpRequest |  |
| putHeader | HttpRequest |  |
| setRetryDelay | HttpRequest |  |
| getCookieStore | BasicCookieStore |  |
| setTimeout | HttpRequest |  |
| sendRequest | HttpResponse |  |
| setContentType | HttpRequest |  |
| getUrl | String |  |
| buildPostHttpUriRequest | HttpUriRequest |  |




