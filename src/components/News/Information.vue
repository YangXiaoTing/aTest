<template>
  <div class="Information">
    <div v-if="false">
      <img :src="require('../../../static/img/information.png')">
    </div>
    <div class="InformationTitle">资讯</div>
    <div class="InformationListWrap" v-if="false">
      <div v-for="(value, index) in dataList" class="InformationList">
        <router-link :to="informationPage+value.id" tag="div" class="InformationItem">
          <img class="InformationItemPic" :src="value.Cover">
          <div class="InformationItemContent">
            <div class="InformationItemContentTitle" v-text="value.Title"></div>
            <div class="InformationItemContentSummary" v-text="value.Summary"></div>
            <div class="InformationItemContentSetupTime">时间：<span v-text="value.SetupTime"></span></div>
          </div>
        </router-link>
      </div>
    </div>
    <div class="InformationListWrap" v-else>
      <div v-for="item in dataList" class="InformationList" :key="item.date" @click="showNews(item)">
          <div>
            <div class="InformationItemContentTitle" v-text="item.title"></div>
            <div class="InformationItemContentSetupTime">时间：<span v-text="item.date"></span></div>
          </div>
      </div>
    </div>
    <el-dialog title="最新咨询"
               size="large"
               :visible.sync="dialogVisible">
      <div v-text="currentNews.date"></div>
      <div v-html="currentNews.content"></div>
    </el-dialog>
  </div>
</template>

<script>
  /* eslint-disable */
  import {Dialog} from 'element-ui'
  import Vue from 'vue'
  Vue.use(Dialog)
  export default {
    name: 'Information',
    data () {
      return {
        informationPage: '/News/InformationDetail/',
        dataList: [
          {
            "title": "以太坊基金会与俄罗斯国家开发银行正式达成合作", "author": "币圈新闻", "date": "2017-09-18 09:55:00", "plate": "", "content": "<div style=\"text-align: right;\"><!--StartFragment--><div style=\"text-align: left;\">致力于推动以太坊发展的非盈利组织以太坊基金会与俄罗斯国家开发银行 Vnesheconombank (VEB)签署了合作协议。&nbsp;<br></div><div><div style=\"text-align: left;\"><br></div><div style=\"text-align: left;\">据昨天宣布的一份联合声明，以太坊基金会将和VEB合作，通过向分布式账簿技术和以太坊平台提供专业培训，来支持它的新的区块链研究中心。&nbsp;</div><div style=\"text-align: left;\"><br></div><div style=\"text-align: left;\">这种合作关系有助于在俄罗斯建立一个以太坊专家社区和建立基于以太坊和其他区块链的项目。&nbsp;</div><div style=\"text-align: left;\"><br></div><div style=\"text-align: left;\">以太坊创始人Vitalik Buterin在声明中表示：&nbsp;</div><div style=\"text-align: left;\"><br></div><div style=\"text-align: left;\">“以太坊和VEB的合作提供了一个独特的机会，可以从事研究和开发利用区块链技术来进行公共管理，并加速将这项技术应用于俄罗斯联邦政府组织。”&nbsp;</div><div style=\"text-align: left;\"><br></div><div style=\"text-align: left;\">上周末， 在Tatarstan举办的名为“区块链：俄罗斯的新石油”活动上，双方正式签署了合作伙伴关系。来自VEB的高级官员和Buterin均出席了此次活动。&nbsp;</div><div style=\"text-align: left;\"><br></div><div style=\"text-align: left;\">此次合作是俄罗斯在全国范围内布局区块链产业的一部分。</div><p></p><h5 style=\"text-align: left;\">本文来源：币圈新闻，如有侵权，请联系平台删除。</h5></div><!--EndFragment--></div><div style=\"text-align: center;\"><!--EndFragment--></div><style>\n@font-face{\nfont-family:\"Times New Roman\";\n}\n\n@font-face{\nfont-family:\"宋体\";\n}\n\n@font-face{\nfont-family:\"Calibri\";\n}\n\n@font-face{\nfont-family:\"Tahoma\";\n}\n\np.MsoNormal{\nmso-style-name:正文;\nmso-style-parent:\"\";\nmargin:0pt;\nmargin-bottom:.0001pt;\nmso-pagination:none;\ntext-align:justify;\ntext-justify:inter-ideograph;\nfont-family:Calibri;\nmso-fareast-font-family:宋体;\nmso-bidi-font-family:'Times New Roman';\nfont-size:10.5000pt;\nmso-font-kerning:1.0000pt;\n}\n\nspan.msoIns{\nmso-style-type:export-only;\nmso-style-name:\"\";\ntext-decoration:underline;\ntext-underline:single;\ncolor:blue;\n}\n\nspan.msoDel{\nmso-style-type:export-only;\nmso-style-name:\"\";\ntext-decoration:line-through;\ncolor:red;\n}\n\ntable.MsoNormalTable{\nmso-style-name:普通表格;\nmso-style-parent:\"\";\nmso-style-noshow:yes;\nmso-tstyle-rowband-size:0;\nmso-tstyle-colband-size:0;\nmso-padding-alt:0.0000pt 5.4000pt 0.0000pt 5.4000pt;\nmso-para-margin:0pt;\nmso-para-margin-bottom:.0001pt;\nmso-pagination:widow-orphan;\nfont-family:'Times New Roman';\nfont-size:10.0000pt;\nmso-ansi-language:#0400;\nmso-fareast-language:#0400;\nmso-bidi-language:#0400;\n}\n@page{mso-page-border-surround-header:no;\n\tmso-page-border-surround-footer:no;}@page Section0{\n}\ndiv.Section0{page:Section0;}</style>" },
          { "title": "拿着比特币去迪拜买房吧", "author": "币圈新闻", "date": "2017-09-18 13:25:28", "plate": "", "content": "<p><!--StartFragment-->本周，两位业界领袖，Baroness Michelle Mone和Douglas Barrowman宣布，将用比特币出售240万平方英尺的迪拜住宅资产。该40层楼的住宅公寓将是位于迪拜科学园区的第一个物业，定价和出售都用加密货币结算。&nbsp;<br></p><h3>第一次用比特币定价的迪拜房地产开发</h3><p>通过与&nbsp;Knox Group和比特币支付处理器Bitpay的合作，将选择1,133套一室和两室的公寓，准备在2019年9月前用于比特币售卖。Aston Development酒店提供独特的享有迪拜山和城市天际线的美景的落地窗视野。此外，该项目由知名建筑师John R Harris＆Partners与Michelle Mone室内设计室设计开发。根据Knox&nbsp;集团的统计，开发区将设有三层咖啡馆，餐馆，超市和精品店。&nbsp;<br>目前，工作室房产的初始价格为33BTC，房地产代理公司表示，早期投资者将获得额外的优惠。此外，还可以使用比特币购买打包的室内设计服务和家具。&nbsp;<br>Mayfair OBE的&nbsp;Baroness Michelle Mone&nbsp;解释说：“作为房地产开发业务的一步，我很高兴能够推出这个规模的项目。“这也是Michelle Mone室内设计公司推出的一个顺理成章的进步，这是我第一次将设计和房产这两个激情融合在一起。”&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>Doug和我都是我们自己的业务领域的开拓者，所以我们当然希望这是与众不同的，独特的和令人兴奋的——不仅仅是房产的世界，而且还是技术的世界。这就是为什么第一此以比特币定价来开发。&nbsp;<br></p><h3>集房产与技术一体</h3><p>Knox集团公司的董事长Douglas Barrowman解释说，该项目已经持续了很长时间。Barrowman认为，迪拜的房地产开发项目是自属一派，他希望成为业内第一个将房产和科技行业融合在一起的。&nbsp;<br>Barrowman说，比特币在短短几年的大幅上涨意味着它是目前世界领先的加密货币。这就是为什么我们第一次以比特币来定价房产的开发。&nbsp;&nbsp;&nbsp;&nbsp;<br>“我相信，随着主流采用，许多人将会跟随我们的领导。正如我在整个职业生涯中所做的一样，就像成为一个引领潮流的人一样，这是一个令人兴奋的事情”。&nbsp;<br>价值2.5亿英镑建设的两座公寓楼和一个购物中心将成为第一个同时最大的以比特币进行定价和结算的项目。&nbsp;Aston Development房地产还详细说明，早期投资者在建设完成后应该会获得9％的投资回报。&nbsp;<br><br>小编闲聊：&nbsp;<br>在大概半个月前，还在相传“一币一嫩模”，到今天只剩下“一币一个馍”了，看来持有比特币是比较稳妥的方式，因为即使不能换成法币，那就拿着比特币去迪拜买房吧。&nbsp;<br>本文来源：币圈新闻，如有侵权，请联系平台删除。&nbsp;<!--EndFragment-->&nbsp;&nbsp;<br></p>" },
          { "title": "人民币买不到iPhone？但是比特币做到了！", "author": "币圈新闻", "date": "2017-09-18 13:31:27", "plate": "", "content": "<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iPhone 8带着iPhone X终于破壳而出，据说还是苹果公司跨时代的作品。这也让我想起了前两年的事件，当时还是iPhone 6出来的时候。下面就是要说的这个事件：&nbsp;</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;人民币买不到iPhone 6，但比特币却做到了，新浪微博上有一则消息引起网友关注，在比特币电商平台币须网上，能直接用比特币买到 iPhone 6。该平台与香港的“iPhone 6频道”店铺合作，以苹果香港的官方价格预订iPhone 6，据店铺的老板事后称，在短短的5个小时内收到订单60多单，相当于人民币近30万，实际支付比特币支付15个订单，由于店铺担心备货不足，不得不中途暂停该活动，并且退掉了其中一些订单。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;有人联系到店铺老板laurance，问到为什么要用比特币支付，安全又如何保证时。Laurance称自己在香港早就接受比特币的支付，原来主要面对欧美用户，这是第一次与比特币电子商务平台合作，也是直面大陆市场，他看中的是币须网采用的多重签名的技术，任何人都拿不走用户的币，这样就消除了用户对店铺的怀疑。至于问到为什么不接受人民币而是接受比特币时，Laurance说并不是不接受人民币，而是他根本没有人民币账户，而比特币可以在全世界流通，在香港也是可以随时兑换成港币或者美元的。&nbsp;</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;比特币在跨境支付方面的确有许多的好处，还有一些网友也通过比特币去英国直接购买iPhone 6。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;比特币能买到iPhone 6的这则消息引起了部分圈外人士以及网络大V对以比特币来进行跨境支付的热情，在币须网用比特币购买iPhone 6 消息发布两天后，任志强转好了一则关于美国接纳比特币金融衍生品的消息，同时著名天使人薛蛮子也在自己的微博里发了一则关于中国的传统电商接受比特币支付的消息。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;对于利用比特币进行跨境支付，这一切才刚刚开始，情况也不是比特币爱好者想像的那样乐观，因为大部分的普通用户手中并不持有比特币，同时也不是每一个国家都有比特币交易所，兑换也非常麻烦。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;当然也有不一样的观点，加密货币电子商务平台“可赢可乐”的运营总监吕明心则认为，加密货币的跨境支付是一种不可阻挡的趋势，虽然很多人手中并不持有比特币，但可用技术的手段去解决它，比特币只作为一种中间的交换媒介，而平台对中间的技术部分进行技术封装 ，普通用户根本感受不到。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;时过境迁，两年大家可以感受到比特币翻了多少倍？现在的一个比特币价格差不多可以买3个iPhone x了，玩币的用户越多也就出现各种各样的数字货币交易所，就需要有人来开发以比特币为首的数字货币交易所。而正好我们有这一块的开发经验，包括比特币背后，以及交易所基层的区块链技术，都是未来探讨研究的方向。\n&nbsp;</p><p>本文来源：币圈新闻，如有侵权，请联系平台删除。&nbsp;&nbsp;</p>" },
          { "title": "华尔街调查：比特币成2017年最受欢迎的投资", "author": "币圈新闻", "date": "2017-09-18 14:31:27", "plate": "", "content": "<p>华尔街调查：比特币成2017年最受欢迎的投资</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;世界顶级基金管理公司的一项调查提供了一个很好的想法：聪明的钱将流向何处。美国银行美林证券(Bank of America Merrill Lynch)在2017年9月的一项针对基金经理的调查显示，比特币是目前最受欢迎的投资，并且拥有大量看涨期权。</p><p>&nbsp;BAML调查的重要性&nbsp;</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;BAML调查是在9月1日至9月7日进行的，在华尔街很受重视。超过200名基金经理参与了这项调查，他们管理着大约6290亿美元的资产。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;因此，这项调查很好地反映了“聪明钱”的流向。尽管华尔街资深人士对比特币前景发表了截然不同的看法，但基金经理似乎相信，很多人都看好比特币。</p><p>&nbsp;“有26%的受访基金经理认为，比特币是目前最受欢迎的投资。”</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;比特币的惊人回报率\n&nbsp;\n比特币在2017年显示出了惊人的回报率，它从年初的950美元上涨到5000美元的巅峰，随后跌至目前的4200美元左右。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;引发比特币价格暴涨的原因很多，比如说，隔离见证的激活，这有助于减少网络的拥堵。此外，亚洲国家温和的法律法规，机构投资者将比特币视为可行的替代资产类别等，也助推了比特币价格的上涨。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;人们担心的是，政府可能会对比特币采取行动，尤其是在中国，这也导致了本月比特币价格的下跌。比特币爱好者认为，随着应用的增加，它将继续升值。</p><p>其他热门交易</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;据BAML调查显示，其他热门交易包括纳斯达克综合指数(Nasdaq Composite Index)的多头交易，以及做空美元(21%)。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在2017年5月至8月期间进行的四次调查中，纳斯达克的多头交易被认为是最受欢迎的投资。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这两项交易在2017年都表现良好，其中纳斯达克综合指数在2017年上涨了20%。</p><p>现在是做空比特币的好时机吗？</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;当大多数人都看好比特币，并且它已经成为最受欢迎的投资的时候，做空比特币的时机来了吗？</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;作为一种受欢迎的投资方式，并不意味着反转即将开始。纳斯达克综合指数(Nasdaq Composite Index)在今年的大部分时间内都被视为受欢迎的投资，但它仍然表现良好。</p><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;即便是反对比特币，甚至将其称之为“欺诈”的人（如摩根大通CEO Jamie Dimon），也不会做空比特币，因为没有人知道比特币价格会走多高。因此，做空比特币可能只是一场赌博，而失败的代价会很惨痛。</p><p><br></p><p>本文来源：币圈新闻，如有侵权，请联系平台删除。</p>" },
          { "title": "将比特币纳入储蓄计划，美国千禧一代缘何这样做？", "author": "巴比特资讯", "date": "2017-09-18 15:31:27", "plate": "", "content": "<p>将比特币纳入储蓄计划，美国千禧一代缘何这样做？\n<br>对于亿万富翁投资者迈克·诺沃格拉茨（Mike Novogratz），以及艾什顿·库奇（Ashton Kutcher）、帕丽斯·希尔顿（Paris Hilton）这些名人而言，比特币已逐渐成为一种主流的投资品。这种不受管制的数字支付系统也被很多人所诟病，但仍然有一批年轻人在畅想未来的无现金社会，并将自己的资金投入到这种数字资产当中。\n<br>他们是与众不同的一类人，在美国人当中，这类群体仅占到了1%，他们不仅听说过比特币，而且还通过智能手机和笔记本电脑进行过相关的交易。更重要的是，一些千禧一代已将比特币视作一种长期储蓄。一些专家们认为，这可能会动摇这个国家的金融机构。\n<br>\n<br>Roshaan Khan，弗吉尼亚联邦大学的一名20岁大学生，他也是这类“千禧一代”的其中一员。最近，Khan投资了比特币以及以太币，并且他也在鼓励自己的朋友做同样的事。\n<br><blockquote>“我所有的净资产都是加密货币，我认为这是还清我的助学贷款的最佳途径，” Khan表示，“我喜欢去中心化的想法，事实上，它能够大大减少腐败以及政治关系。这个想法对我很有吸引力……其也不必经过银行。”\n</blockquote>Andreas M. Antonopoulos，《精通比特币》以及《互联网货币》的作者，他非常熟悉千禧一代身上存在的不信任感。他说，互联网货币的概念，不仅仅是吸引着千禧一代，而且这种系统也不会背叛他们。\n<br><blockquote>“当你走近那些对社会机构已失望的千禧一代，你会发现，他们已不再信任任何人，” Antonopoulos说，“他们记得2008年发生的事，因为这是他们第一次遭遇大危机，很多千禧一代在那个时期无法找到工作。而他们，也没有看到有银行家被判入监狱。”\n</blockquote>现在，千禧一代开始选择他们自己的方式。\n<br><blockquote>“通过投资这种新技术来经营自己的储蓄计划，让我感觉甚好， ”年仅24岁的Emil Thorsplass表示，他是一位来自挪威的音乐家。“我仍然会通过银行账户来定期投养老基金并支付账单，但加密货币投资已成为了我的储蓄计划的一部分。”\n</blockquote>然而，数字货币也面临着大量的批评。一些传统投资者认为，比特币虽然没有固有的缺陷，但作为一种数字支付方式，它不值得投资，因其的波动性过大，且没有中央机构或政府的支持。Antonopoulos则回应称这种说法是“跛脚”的，他认为成熟的投资者可以把波动性较大的投资品列入自己的投资组合。\n<br><blockquote>“你可以对比特币进行批评，它显然是存在风险的，这种技术的存在时间大约只有9年，在很大程度上，它还处在实验阶段，” Antonopoulos说，“如果将其纳为投资组合的一部分，其存在较低的可能会给你带来很高的回报，但其完全崩溃的可能性，也是不容忽视的。如果你愿意抓住这个机会，这可能会给你的人生带来很大的变化，尤其对年轻人而言。”<br>\n“对于波动性，我不再像以前那样紧张，” Thorsplass表示，自2015年以来，这位年轻人在数字货币当中已投入了5000美元。“我习惯于冒险，所以当我的直觉告诉我应该这样做时，我喜欢扣动扳机。”\n</blockquote>Khan自两个月前开始投资数字货币以来，其投资回报率达到了40%，他也表达了类似的看法。\n<br><blockquote>“也许是我刚涉入这个领域，但没有其他东西能比它更让我兴奋了，股票市场已变得极其无聊。对于一个囊中羞涩的大学生来说，在庞大的股票市场当中没有作为可言。”\n</blockquote>但重要的是，任何交易比特币的人都要明白，虽然比特币本身可能不受监管，但与其进行交换的法币是受到很多管制的。\n<br><blockquote>“关于拥有或使用比特币，或者任何其他的加密货币，其本身不会触犯任何法律，你只需要在投资或使用它们前掌握一些相关知识，” 加密货币律师Tyson Cros表示，“但你可能很容易在税收方面陷入麻烦。”\n</blockquote>他继续说，“我认为美国国税局已在紧盯这个领域了，很多加密货币交易可能并没有纳税。我认为这种日子要离我们而去了，如果有人打算投资比特币或其他加密货币，我会警告他们不要想着逃税漏税，因为目前国税局有很多工具可以检测到这些行为。”\n<br>有一件事是可以肯定的：加密货币的概念不可能很快消失。即使比特币明天突然消失了，一种新的、更好的数字货币也会取代它的位置。\n<br>“比特币所展现给我们的是，其技术可用于创建一个竞争性产品，它能够和国家的法币相提并论，甚至在某些方面会更好，” Antonopoulos说，“它为竞争打开了大门，这将决定我们前进的方向。当新产品进入市场时会发生什么？一场浩劫。”\n<br><blockquote>“现在，市场上就出现了选择，而千禧一代就是在行使选择权。\n</blockquote>\n<br>原文：\n<br>https://www.coindesk.com/indian-central-bank-studies-fiat-cryptocurrency-for-digital-rupee/\n<br>作者：Rachel Rose O'Leary\n<br>编译：Wendy\n<br>稿源（译）：巴比特资讯（http://www.8btc.com/indian-central-bank-digital-rupee)\n<br>版权声明：作者保留权利。文章为作者独立观点，不代表平台立场。&nbsp;<br></p>" },
          { "title": "央行孙国峰：ICO不同于区块链，穿透式监管更适合中国", "author": "第一财经", "date": "2017-09-18 16:47:04", "plate": "", "content": "<p><h3>央行孙国峰：ICO不同于区块链，穿透式监管更适合中国\n</h3><blockquote> [美国一些金融科技监管经验很值得中国借鉴，特别是其穿透式监管、功能监管方面。而监管沙盒，总体并不适合在中国大范围普遍开展]<br>\n[2017年初至今，整个虚拟货币市场价值增长了811%，相当于1460亿美元。ICO确实存在很大的泡沫。]\n</blockquote>\n<br>日前，中国人民银行金融研究所所长孙国峰在接受央行旗下媒体专访时明确表示，叫停ICO（首次代币发行）是十分必要和及时的，必须把区块链技术和ICO区分开来。\n<br>他还表示，金融科技具有很强的风险特征，必须加强监管，美国对金融科技的穿透式监管、功能监管方面经验值得借鉴，但监管沙盒并不合适中国。\n<br>&nbsp;\n<br><h4>区块链不等同于ICO\n</h4>&nbsp;\n<br>2016年4月开始，央行牵头多部委联合开展互联网金融风险专项整治工作，10月13日国务院正式下发实施方案。在一年多的时间里，专项整治工作小组先后对P2P网络借贷、第三方支付等领域频出重拳。尤其是近期对ICO的监管整治，并没有采取一贯的“软着陆”而是选择了“急刹车”，定性为非法金融活动，并“一刀切”取消在国内的发行和交易。\n<br>孙国峰在采访中对叫停ICO给出解释，实际上ICO涉嫌非法发售代币票券、非法发行证券以及非法集资、金融诈骗、传销等违法犯罪活动，当前，叫停ICO是十分必要和及时的。但是这并不妨碍相关的金融科技公司、行业机构、技术公司去继续研究区块链技术，区块链本身是好技术，并不是只有通过ICO才能进行区块链技术研究，还可以通过各种技术进行研究。\n<br>因此，要把区块链技术和ICO区分开来，区块链技术可以运用于很多领域、场景，包括一些社会管理领域场景，不应当将区块链和ICO画等号，需要进一步拓宽研究和发展区块链技术的视野。\n<br>在监管政策落地后，上周末北京举行了一场区块链会议，对区块链“回归”和发展进行了讨论。\n<br>与会专家也表示，在此前ICO融资逐步上升甚至取代风投成为新科技融资主要渠道的同时，2017年初至今，整个虚拟货币市场价值增长了811%，相当于1460亿美元。ICO确实存在很大的泡沫。而且，很多ICO融资流入了债券、有色金属、股票中，ICO是不是在支持科技发展需要打上一个问号。ICO搅乱金融市场，区块链技术也会受到负面影响。\n<br>&nbsp;\n<br><h4>穿透式监管更适合中国\n</h4>&nbsp;\n<br>孙国峰指出，金融科技还是具有很强的风险特征，必须要加强监管。他建议，对于国内金融科技监管要将微观功能监管与宏观审慎管理相结合。美国一些金融科技监管经验很值得中国借鉴，特别是其穿透式监管、功能监管方面。而监管沙盒，总体并不适合在中国大范围普遍开展。\n<br>孙国峰表示，金融科技本身的金融属性决定了其有很强的风险特征。从目前的风险来看，一是来自金融科技自身的风险，二是金融科技存在造成金融体系金融风险加大的因素。一方面，金融科技使得金融风险更加具有隐蔽性、传播速度更快、影响范围更广，增加了金融系统性风险；另一方面，金融科技使金融业“脱媒风险”加大；此外，金融科技还会涉及金融消费者保护的问题。总体来说，金融科技还是具有很强的风险特征，必须要加强监管。\n<br>目前，国际上金融科技监管模式大致可以分为两类，一类是一些相对小型开放的经济体并且是国际金融中心，比如英国、新加坡。这些国家由于自身市场比较小，金融科技发展产生的风险隐患并不是很突出，同时肩负着国际金融中心发展的任务，会采取一些鼓励措施，包括引入监管沙盒；另一类是一些大型经济体且金融市场特别大，比如美国、中国。美国发展金融科技在技术上具有一些领先优势，且监管严格。而中国在金融科技运用场景方面虽明显领先，但也存在监管模糊地带，特别重要的是个人数据保护不及美国完善。\n<br>在他看来，美国一些金融科技监管经验很值得中国借鉴，特别是其穿透式监管、功能监管方面。在美国，不管金融科技以何种形态出现，均根据涉及的金融业务性质纳入到相应的金融监管体系之中，比如P2P，有些业务涉及产权变化，由美国证监会进行监管。美国财政部对货币服务机构进行监管，每个州都有货币转移法，对货币转移要求在州政府监管机构进行注册登记，此外美国还有联邦消费者保护法、联邦金融消费者保护局，从行为监管的角度保护相关消费者的合法权益。\n<br><blockquote>“至于监管沙盒，作为一个国际经验，也不排除考虑在个别领域进行试点，但总体并不适合在中国大范围普遍开展。”\n</blockquote>孙国峰指出，中国金融科技现在主要的问题还是监管不足。\n<br>从国际经验看，监管沙盒实施对象都是一些初创型企业，金融科技自我发展动力不足，需要鼓励发展。相反，我国市场比较大，金融科技机构相对来说比较容易盈利，自身发展动力强，在此背景下如果再实施监管沙盒，很多大中小型金融科技机构都会来申请，可能容纳不下如此多的机构。\n<br>孙国峰认为，中国金融科技监管要注重微观功能监管和宏观审慎管理相结合。微观功能监管采取穿透式监管，根据金融科技的金融特征，按照相关业务的类别由相关监管当局进行监管，实现监管全覆盖，避免监管空白。宏观审慎管理是把金融科技纳入到宏观审慎管理框架当中，完善支付机构客户备付金集中制度。他还提出，应当把具有系统重要性的金融科技公司纳入宏观审慎管理框架。\n<br>原文载于：http://www.yicai.com/news/5344227.html\n<br>版权声明：作者保留权利。文章为作者独立观点，不代表本平台立场。&nbsp;</p>" }
        ],
        dialogVisible: false,
        currentNews: {}
      }
    },
    methods: {
      showNews(item) {
        this.currentNews = item
        this.dialogVisible = true
      }
    }
  }
</script>

<style scoped>
  .Information{
    color: #fff;
    width: 988px;
    height: 800px;
    margin: 86px auto;
    font-size: 14px;
  }
  .InformationTitle{
    font-size: 24px;
    border-bottom: 1px solid rgba(255,255,255,.3);
    padding: 0 0 10px 14px;
    margin-top: 18px;
  }
  .InformationList{
    padding: 10px 0 20px;
    border-bottom: 1px solid rgba(255,255,255,.3);
  }
  .InformationItem{
    padding: 10px 0;
    overflow: hidden;
    cursor: pointer;
  }
  .InformationItemPic{
    width: 254px;
    height: 184px;
    float: left;
  }
  .InformationItemContent{
    float: left;
    padding-top: 18px;
    margin-left: 30px;
    width: 702px;
    overflow: hidden;
  }
  .InformationItemContentTitle{
    font-size: 18px;
    color: skyblue;
    cursor: pointer;
  }
  .InformationItemContentTitle:hover{
    color: powderblue;
  }
  .InformationItemContentSummary{
    margin: 13px 0 24px;
    max-height: 74px;
    box-sizing: border-box;
    overflow: hidden;
    text-overflow : ellipsis
  }
  .InformationItemContentSetupTime{
    font-size: 12px;
    color: #bbb;
  }
</style>

<style>
  .NoticeListPagination .el-pager li{
    border: none;
    background:transparent;
  }
  .NoticeListPagination .el-pager li.active{
    border-color: transparent;
  }
  .NoticeListPagination .el-pagination button{
    background: transparent;
    border: none;
  }
  .NoticeListPagination .el-pagination__total{
    color: #fff
  }
</style>
