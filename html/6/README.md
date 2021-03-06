# 简述前端性能优化

## 页面内容方面

1. 通过文件合并、css 雪碧图、使用 base64 等方式来减少 HTTP 请求数，避免过多的请求造成等待的情况；
2. 通过 DNS 缓存等机制来减少 DNS 的查询次数；
3. 通过设置缓存策略，对常用不变的资源进行缓存；
4. 通过延迟加载的方式，来减少页面首屏加载时需要请求的资源，延迟加载的资源当用户需要访问时，再去请求加载；
5. 通过用户行为，对某些资源使用预加载的方式，来提高用户需要访问资源时的响应速度；

## 服务器方面

1. 使用 CDN 服务，来提高用户对于资源请求时的响应速度；
2. 服务器端自用 Gzip、Deflate 等方式对于传输的资源进行压缩，减少传输文件的体积；
3. 尽可能减小 cookie 的大小，并且通过将静态资源分配到其他域名下，来避免对静态资源请求时携带不必要的 cookie；