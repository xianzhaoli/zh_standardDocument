# zh_standardDocument
国家标准文档抓取

难点1：<br/>
  问题：网站每次点击预览或者下载时需要输入验证码，通过研究发现只要获取一次验证码并且输入后就有一次下载机会 <br/>
  解决：每次下载前请求一次验证码并且通过文字识别图片识别出验证码然后调用验证接口验证，验证后可直接下载。
<br />
难点2：<br/>
  问题：只能够在线预览的文件PDF，通过开发者工具查看发现pdf被拆分成图片并分块混淆展示， <br/>
  解决：获取每个page的背景图片并通过120*169像素切分，通过元素中的position和class中的pdf-0-1（例如）计算出原始位置并进行合并。
