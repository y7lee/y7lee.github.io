---
layout: post
title: "What hanppend on-chain when you mint a"
description: "作为新接触web3 的人，钱包转账，合约交互等问题常常让我们难以理解，尤其是其表面的逻辑和背后的数据流通，常常让人感到疑惑。这里将基于一个简单的MINT的案例，利用链上数据工具，追踪该行为在链上留下的痕迹，解释当你MINT一个"
date: 2024-04-07
category: blockchain
tags: [blockchain onchain-data tutorial]
---
<h1 id="what-happened-when-mint-a-bytepass">What happened when mint a Bytepass</h1>
<p>作为新接触web3 的人，钱包转账，合约交互等问题常常让我们难以理解，尤其是其表面的逻辑和背后的数据流通，常常让人感到疑惑。这里将基于一个简单的转账和合约交互的案例，利用链上数据工具，追踪这些活动在链上留下的踪迹，帮助大家更好的理解WEB3中以太坊生态下的合约交互的逻辑和方法。
这里将使用</p>
<h1 id="场景">场景</h1>
<p>首先介绍我做了什么</p>
<h1 id="链上数据追踪">链上数据追踪</h1>
<h2 id="转账">转账</h2>
<div class="highlight"><pre tabindex="0" style="color:#f8f8f2;background-color:#272822;-moz-tab-size:4;-o-tab-size:4;tab-size:4;"><code class="language-sql" data-lang="sql"><span style="display:flex;"><span><span style="color:#66d9ef">SELECT</span>
</span></span><span style="display:flex;"><span>  <span style="color:#f92672">*</span>
</span></span><span style="display:flex;"><span><span style="color:#66d9ef">FROM</span> optimism.transactions x
</span></span><span style="display:flex;"><span><span style="color:#66d9ef">WHERE</span>
</span></span><span style="display:flex;"><span>  x.<span style="color:#e6db74">&#34;from&#34;</span> <span style="color:#66d9ef">IN</span> (<span style="color:#ae81ff">0</span>xE668a961CaDc3e4526e5583AEe9C6d460820315e)
</span></span><span style="display:flex;"><span>  <span style="color:#66d9ef">OR</span> x.<span style="color:#e6db74">&#34;to&#34;</span> <span style="color:#66d9ef">IN</span> (<span style="color:#ae81ff">0</span>xE668a961CaDc3e4526e5583AEe9C6d460820315e)
</span></span></code></pre></div><h2 id="合约交互">合约交互</h2>
<h2 id="heading"></h2>
