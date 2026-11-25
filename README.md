<img width="653" height="317" alt="image" src="https://github.com/user-attachments/assets/4861949e-4ac9-4026-bc48-f3a80e6db80e" />
<h1>局域网桥 <a href="https://j.lianghua.fun/">evgate</a>：把手机网络共享给身边设备</h1>

<p>电脑、平板、电视、游戏机——只要填一个代理地址就能上网。</p>

<p>手机开 HTTP / HTTPS / SOCKS5 代理，同一 WiFi 或热点下的设备直接可用，PAC 一行地址搞定。<strong>免 root，对端设备无需安装任何软件。</strong></p>

<p><a href="https://github.com/huayuanhaoting/evgate/releases/tag/evgate">下载 APK</a></p>

<hr>

<h2>能共享给哪些设备</h2>

<table>
  <thead>
    <tr><th>设备</th><th>填在哪</th></tr>
  </thead>
  <tbody>
    <tr><td>Windows / Mac 电脑</td><td>系统设置 → 网络 → 代理 → HTTP 代理</td></tr>
    <tr><td>平板 / 另一台手机</td><td>WiFi 详情 → 代理 → 手动</td></tr>
    <tr><td>智能电视 / 机顶盒</td><td>网络设置 → 代理服务器</td></tr>
    <tr><td>游戏机（PS / Switch）</td><td>网络设置 → 代理服务器 → 手动</td></tr>
    <tr><td>车机 / 老设备</td><td>只要能填 HTTP 代理就能连</td></tr>
  </tbody>
</table>

<blockquote>以上设备都无需装软件，填一个地址就行。</blockquote>

<hr>

<h2>三步开始用</h2>

<p>手机负责上网，其他设备只管连手机。</p>

<ol>
  <li><strong>点「启动共享」</strong><br>按钮变成「停止共享」即为已开始。</li>
  <li><strong>记下地址</strong><br>形如 <code>192.168.1.6:8080</code>，应用内按网卡列出。</li>
  <li><strong>填到设备</strong><br>按上表打开代理设置，填入 HTTP 代理一栏。</li>
</ol>

<blockquote>
  <p>支持 PAC 的设备填 <code>http://手机地址:8080/proxy.pac</code> 更省事。<br>
  换了 WiFi 地址会变，需要重填。</p>
</blockquote>

<hr>

<h2>协议与端口</h2>

<table>
  <thead>
    <tr><th>协议</th><th>默认端口</th><th>说明</th></tr>
  </thead>
  <tbody>
    <tr><td>HTTP 正向代理</td><td>8080</td><td>浏览器、系统代理直接填</td></tr>
    <tr><td>HTTPS 隧道（CONNECT）</td><td>8080</td><td>与 HTTP 共用端口，纯透传，无需装证书</td></tr>
    <tr><td>SOCKS5 / 4A / 4</td><td>1080</td><td>同端口兼容三个版本，SOCKS5 支持 UDP 中继</td></tr>
    <tr><td>PAC 自动配置</td><td>8080</td><td>地址为 <code>http://手机地址:8080/proxy.pac</code></td></tr>
  </tbody>
</table>

<p>认证可选，HTTP 与 SOCKS5 共用一套用户名密码；默认双栈监听（IPv4 + IPv6），也可只绑指定网卡。并发默认 128 条，可按客户端 IP 限速与设置每日额度，日志可导出 CSV / JSON。</p>

<blockquote><strong>热点共享</strong>：需先在系统设置里打开「个人热点」，再使用热点网段的地址。</blockquote>

<hr>

<h2>界面</h2>

<ul>
  <li><strong>主界面</strong>：启动共享 + 实时上下行流量与连接数。</li>
  <li><strong>协议与端口</strong>：HTTP 8080、SOCKS 1080。</li>
  <li><strong>按网卡列出地址</strong>：HTTP、SOCKS 与 PAC 地址一目了然，PAC 可直接复制。</li>
</ul>

<hr>

<h2>安全</h2>

<ul>
  <li><strong>纯本地转发</strong>：没有云端、没有中转，流量不经过任何人。</li>
  <li><strong>不收集数据</strong>：无账号、无统计、无广告，零第三方依赖。</li>
  <li><strong>看不到加密内容</strong>：HTTPS 传什么它看不见，只搬字节。</li>
</ul>
