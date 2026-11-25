<img width="653" height="317" alt="image" src="https://github.com/user-attachments/assets/4861949e-4ac9-4026-bc48-f3a80e6db80e" />
<!-- ===================== 语言切换 ===================== -->
<p>
  <a href="#zh">中文</a> | <a href="#en">English</a>
</p>

<hr>

<!-- ===================== 中文版 ===================== -->
<section lang="zh-CN">

<h1 id="zh">局域网桥 <a href="https://j.lianghua.fun/">evgate</a>：把手机网络 / VPN 共享给身边设备（免 root 的 Android 热点代理服务器）</h1>

<p>电脑、平板、电视、游戏机——只要填一个代理地址就能上网。</p>

<p>手机开 HTTP / HTTPS / SOCKS5 代理，同一 WiFi 或热点下的设备直接可用，PAC 一行地址搞定。<strong>免 root，对端设备无需安装任何软件。</strong></p>

<p>适合这些场景：<strong>共享手机 VPN 连接</strong>、<strong>把手机当热点代理服务器（Android hotspot proxy server）</strong>、<strong>免 root 共享网络</strong>，让电视、游戏机、车机等无法直连 VPN 的设备也走上手机的网络出口。</p>

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

<p>手机负责上网（含手机已连的 VPN），其他设备只管连手机。</p>

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

<hr>

<h2 id="zh-keywords">局域网桥 evgate</h2>

<p>共享手机 VPN、免 root 共享 VPN、把手机 VPN 共享给电脑 / 电视 / 游戏机、Android 热点代理服务器、手机当代理、局域网代理共享、SOCKS5 热点代理、PAC 自动配置。</p>

<p><a href="#zh">↑ 返回顶部</a></p>

</section>

<hr>

<!-- ===================== English ===================== -->
<section lang="en">

<h1 id="en"><a href="https://j.lianghua.fun/">evgate</a> — Share Your Phone's Network / VPN with Nearby Devices (Root-Free Android Hotspot Proxy Server)</h1>

<p>Computers, tablets, TVs, game consoles — just fill in one proxy address and you're online.</p>

<p>Run an HTTP / HTTPS / SOCKS5 proxy on your phone; any device on the same WiFi or hotspot can use it directly, and a single PAC URL handles everything. <strong>No root, and no software to install on client devices.</strong></p>

<p>Great for: <strong>sharing your phone's VPN connection</strong>, <strong>turning your phone into an Android hotspot proxy server</strong>, <strong>sharing a VPN without root</strong> — so TVs, consoles, car head units and other devices that can't connect to a VPN directly can still route through your phone's network.</p>

<p><a href="https://github.com/huayuanhaoting/evgate/releases/tag/evgate">Download APK</a></p>

<hr>

<h2>Which Devices Can Share It</h2>

<table>
  <thead>
    <tr><th>Device</th><th>Where to Enter It</th></tr>
  </thead>
  <tbody>
    <tr><td>Windows / Mac computer</td><td>System Settings → Network → Proxy → HTTP Proxy</td></tr>
    <tr><td>Tablet / another phone</td><td>WiFi details → Proxy → Manual</td></tr>
    <tr><td>Smart TV / set-top box</td><td>Network settings → Proxy server</td></tr>
    <tr><td>Game console (PS / Switch)</td><td>Network settings → Proxy server → Manual</td></tr>
    <tr><td>Car head unit / legacy device</td><td>Any device that accepts an HTTP proxy works</td></tr>
  </tbody>
</table>

<blockquote>None of these devices need any software — just fill in one address.</blockquote>

<hr>

<h2>Get Started in 3 Steps</h2>

<p>Your phone handles the internet (including any VPN it's connected to); other devices just connect to the phone.</p>

<ol>
  <li><strong>Tap "Start Sharing"</strong><br>When the button changes to "Stop Sharing", it's running.</li>
  <li><strong>Note the address</strong><br>Something like <code>192.168.1.6:8080</code>, listed per network interface in the app.</li>
  <li><strong>Enter it on the device</strong><br>Open the proxy settings per the table above and fill it into the HTTP proxy field.</li>
</ol>

<blockquote>
  <p>Devices that support PAC can simply use <code>http://phone-address:8080/proxy.pac</code>.<br>
  The address changes when you switch WiFi, so re-enter it as needed.</p>
</blockquote>

<hr>

<h2>Protocols &amp; Ports</h2>

<table>
  <thead>
    <tr><th>Protocol</th><th>Default Port</th><th>Notes</th></tr>
  </thead>
  <tbody>
    <tr><td>HTTP forward proxy</td><td>8080</td><td>Use directly in browsers and system proxy settings</td></tr>
    <tr><td>HTTPS tunnel (CONNECT)</td><td>8080</td><td>Shares the port with HTTP, pure passthrough, no certificate needed</td></tr>
    <tr><td>SOCKS5 / 4A / 4</td><td>1080</td><td>Three versions on one port; SOCKS5 supports UDP relay</td></tr>
    <tr><td>PAC auto-config</td><td>8080</td><td>URL: <code>http://phone-address:8080/proxy.pac</code></td></tr>
  </tbody>
</table>

<p>Optional authentication (one username/password shared by HTTP and SOCKS5); dual-stack listening by default (IPv4 + IPv6), or bind to a specific interface only. Default concurrency is 128 connections, with per-client-IP rate limits and daily quotas; logs exportable as CSV / JSON.</p>

<blockquote><strong>Hotspot sharing</strong>: first enable "Personal Hotspot" in system settings, then use the hotspot subnet address.</blockquote>

<hr>

<h2>Interface</h2>

<ul>
  <li><strong>Main screen</strong>: start sharing + live upstream/downstream traffic and connection count.</li>
  <li><strong>Protocols &amp; ports</strong>: HTTP 8080, SOCKS 1080.</li>
  <li><strong>Per-interface addresses</strong>: HTTP, SOCKS and PAC addresses at a glance — copy the PAC directly.</li>
</ul>

<hr>

<h2>Security</h2>

<ul>
  <li><strong>Purely local forwarding</strong>: no cloud, no relay — traffic never passes through anyone else.</li>
  <li><strong>No data collection</strong>: no accounts, no analytics, no ads, zero third-party dependencies.</li>
  <li><strong>Can't see encrypted content</strong>: HTTPS payloads are invisible to it — it only moves bytes.</li>
</ul>

<hr>

<h2 id="en-keywords"><a href="https://j.lianghua.fun/">evgate</a></h2>

<p>Share phone's VPN connection, share VPN without root, Android hotspot proxy server, use phone as proxy server, LAN proxy sharing, SOCKS5 hotspot proxy, PAC auto-config.</p>

<p><a href="#en">↑ Back to top</a></p>

</section>
