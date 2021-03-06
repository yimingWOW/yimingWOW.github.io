# Anonymity区块链的匿名性
1. 比特币不具备匿名性
    - 尽管比特币使用不具备自然语义的公钥哈希值作为身份证明，但是它无法做到完全匿名
    - 一旦使用者将其变卖为法币，公钥哈希值总是可以关联到使用者的社会真实身份
    - 因此比特币只是一个化名系统
    
2. 匿名的几种方法
    1. 隐形地址
        - 收款人公布公钥 $g_x$, x为私钥，地址函数为$H(g_x)$
        - 汇款人取一个随机数r，计算$(g_x)r=g_{xr}$
        - 收款人想办法获取该随机数，即可将$g_{xr}$中的比特币取出
        - 所谓隐形地址就是使用非对称加密方法将汇款地址做了加密，这里的随机数r对于收款人来讲，就是他获取汇款的密码
        - 将收款地址做了加密，好处是收款地址是由汇款人提供的，只要收款人知道r，总是能得到收款地址
        - 但是只要收款人将这笔比特币提现，就总是可以追踪出他的社会身份
    
    b.混币Mixing
    
    - 首先构建一个混币交易池。鲍勃将他的钱汇入交易池指定的地址中，混币服务商将其他地址的比特币转到鲍勃想要收款的地址中
    - 如果鲍勃的钱最初是一笔赃款，比如盗取来的比特币。经过混币交易池后，鲍勃的一个合法地址得到了从无数个合法地址转来的比特币。这样他的钱就被洗白了
    - 混币服务商可能是有正规业务的商户，比如支持比特币交易的服装店或者零售超市，他们将鲍勃的赃款可能被支付给成千上万顾客。这样一笔赃款就淹没在人民群众的汪洋大海中。
    - 混币仍然是有风险的。比如，鲍勃向交易池转了500个比特币。在这笔转账完成后，鲍勃用他经常使用的地址接收到了500个比特币，那么他的这500个比特币实在是有很大嫌疑是当初那笔赃款。聪明的洗钱嫌疑犯应该转入500个比特币，最后只向混币服务商索要5个，那么司法机关就很难怀疑到他头上了哈哈。
    - 提供混币服务的人，俗称洗钱的人
