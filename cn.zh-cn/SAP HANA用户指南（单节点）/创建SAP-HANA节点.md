# 创建SAP HANA节点<a name="saphana_02_0024"></a>

SAP HANA运行在HANA云服务器上。需要根据部署场景，创建一台或多台HANA云服务器，用于部署SAP  HANA软件。

请参见方案和数据规划相关章节，确定HANA云服务器数量及相关规划信息。

## 操作步骤<a name="section28521827213651"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)，选择区域和项目。
3.  在左侧导航栏，单击![](figures/002-2.png)，选择“计算 \> 弹性云服务器“，进入“弹性云服务器“管理界面。
4.  在右侧界面中，单击“购买弹性云服务器“，系统弹出购买弹性云服务器的界面。
5.  根据界面提示，配置HANA云服务器基础信息，如[表1](#table15048540213231)所示。

    **表 1**  HANA云服务器基础配置

    <a name="table15048540213231"></a>
    <table><thead align="left"><tr id="row36609903213231"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p11338703213231"><a name="p11338703213231"></a><a name="p11338703213231"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p46019721213231"><a name="p46019721213231"></a><a name="p46019721213231"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row49191815173125"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p56583456173136"><a name="p56583456173136"></a><a name="p56583456173136"></a>计费模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p19857206173136"><a name="p19857206173136"></a><a name="p19857206173136"></a>按需求选择计费方式，推荐使用“包年/包月”。</p>
    </td>
    </tr>
    <tr id="row23050208213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p43115582213231"><a name="p43115582213231"></a><a name="p43115582213231"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p2701244213231"><a name="p2701244213231"></a><a name="p2701244213231"></a>指定云服务器所在的可用分区，必须是支持SAP HANA的可用分区，请根据实际需要选择。</p>
    </td>
    </tr>
    <tr id="row66682020917"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p0670201392"><a name="p0670201392"></a><a name="p0670201392"></a>CPU架构</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p2671120095"><a name="p2671120095"></a><a name="p2671120095"></a>根据实际选择“x86计算”或“鲲鹏计算”。</p>
    <a name="ul144564131810"></a><a name="ul144564131810"></a><ul id="ul144564131810"><li>X86计算：x86 CPU架构采用复杂指令集（CISC），CISC指令集的每个小指令可以执行一些较低阶的硬件操作，指令数目多而且复杂，每条指令的长度并不相同。由于指令执行较为复杂所以每条指令花费的时间较长。</li><li>鲲鹏计算：鲲鹏  CPU架构采用RISC精简指令集（RISC），RISC是一种执行较少类型计算机指令的微处理器，它能够以更快的速度执行操作，使计算机的结构更加简单 合理地提高运行速度，相对于X86 CPU架构具有更加均衡的性能功耗比。鲲鹏的优势是高密度低功耗，可以提供更高的性价比。</li></ul>
    </td>
    </tr>
    <tr id="row45743662213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p6125286213231"><a name="p6125286213231"></a><a name="p6125286213231"></a>规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p42732086153926"><a name="p42732086153926"></a><a name="p42732086153926"></a>单击“超大内存型”，请根据实际需要选择，规格可参见<a href="SAP-HANA节点规划.md">SAP HANA节点规划</a>中的说明。</p>
    </td>
    </tr>
    <tr id="row35173131213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p27861758213231"><a name="p27861758213231"></a><a name="p27861758213231"></a>镜像</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p44344974213231"><a name="p44344974213231"></a><a name="p44344974213231"></a>请选择<span class="parmvalue" id="parmvalue42209921213231"><a name="parmvalue42209921213231"></a><a name="parmvalue42209921213231"></a>“市场镜像”</span>，单击“选择镜像”，在搜索框输入关键词“SAP”，选择合适的云服务器镜像。</p>
    </td>
    </tr>
    <tr id="row50316870213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p48122725213231"><a name="p48122725213231"></a><a name="p48122725213231"></a>系统盘</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p4699356994429"><a name="p4699356994429"></a><a name="p4699356994429"></a><span class="keyword" id="keyword13338175120815"><a name="keyword13338175120815"></a><a name="keyword13338175120815"></a>单节点</span>（无HA或HA场景）部署时，共需要一块系统盘和多块用户数据盘。</p>
    <p id="p1235031294247"><a name="p1235031294247"></a><a name="p1235031294247"></a>磁盘具体要求请参见<a href="SAP-HANA节点规划.md">SAP HANA节点规划</a>的说明。</p>
    <p id="p2659803510710"><a name="p2659803510710"></a><a name="p2659803510710"></a>若有特殊需求需要额外的磁盘，可单击<span class="uicontrol" id="uicontrol5651416510711"><a name="uicontrol5651416510711"></a><a name="uicontrol5651416510711"></a>“增加一块数据盘”</span>增加磁盘。</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“下一步：网络配置”。
7.  根据界面提示，配置HANA云服务器网络信息，如[表2](#table16563101213313)所示。

    **表 2**  HANA云服务器网络配置

    <a name="table16563101213313"></a>
    <table><thead align="left"><tr id="row11563111223120"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p1756341273112"><a name="p1756341273112"></a><a name="p1756341273112"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p1563112103116"><a name="p1563112103116"></a><a name="p1563112103116"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row9564101214317"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1564612173112"><a name="p1564612173112"></a><a name="p1564612173112"></a>网络</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p18564312103110"><a name="p18564312103110"></a><a name="p18564312103110"></a>请使用<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>中对应的VPC、子网信息。</p>
    </td>
    </tr>
    <tr id="row9564141219315"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p15641127313"><a name="p15641127313"></a><a name="p15641127313"></a>扩展网卡</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p656471253117"><a name="p656471253117"></a><a name="p656471253117"></a>请根据<a href="网络信息规划.md">网络信息规划</a>确定网卡个数。</p>
    <p id="p1564171212317"><a name="p1564171212317"></a><a name="p1564171212317"></a>若需添加，可单击<span class="uicontrol" id="uicontrol556415128313"><a name="uicontrol556415128313"></a><a name="uicontrol556415128313"></a>“增加一块网卡”</span>增加网卡。</p>
    <div class="note" id="note1456441219316"><a name="note1456441219316"></a><a name="note1456441219316"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul1156531211318"></a><a name="ul1156531211318"></a><ul id="ul1156531211318"><li>单节点部署（无HA）：无需添加扩展网卡。</li><li>单节点部署（HA）：添加扩展网卡后，执行去勾选“安全组不生效”。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="row856514125316"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p155651312153115"><a name="p155651312153115"></a><a name="p155651312153115"></a>安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p85651122313"><a name="p85651122313"></a><a name="p85651122313"></a>请使用<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>中对应的安全组。</p>
    </td>
    </tr>
    <tr id="row13565151273110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1456551223119"><a name="p1456551223119"></a><a name="p1456551223119"></a>弹性公网IP</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p156591211318"><a name="p156591211318"></a><a name="p156591211318"></a>选择“暂不购买”。</p>
    </td>
    </tr>
    </tbody>
    </table>

8.  单击“下一步：高级配置”。
9.  根据界面提示，配置HANA云服务器高级信息，如[表3](#table17181316193420)所示。

    **表 3**  HANA云服务器高级配置

    <a name="table17181316193420"></a>
    <table><thead align="left"><tr id="row1518111693415"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p41811516163411"><a name="p41811516163411"></a><a name="p41811516163411"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p618114164341"><a name="p618114164341"></a><a name="p618114164341"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row125915551599"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p14186616173411"><a name="p14186616173411"></a><a name="p14186616173411"></a>云服务器名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p17186101663413"><a name="p17186101663413"></a><a name="p17186101663413"></a>云服务器名称。</p>
    <p id="p111861616143418"><a name="p111861616143418"></a><a name="p111861616143418"></a>在批量创建云服务器时，每台云服务器的<span class="parmname" id="parmname2186201633417"><a name="parmname2186201633417"></a><a name="parmname2186201633417"></a>“云服务器名称”</span>会根据填写的参数值自动递增。比如填写的是<span class="parmvalue" id="parmvalue1618661618340"><a name="parmvalue1618661618340"></a><a name="parmvalue1618661618340"></a>“hana”</span>，第一台云服务器为<span class="parmvalue" id="parmvalue15186316153414"><a name="parmvalue15186316153414"></a><a name="parmvalue15186316153414"></a>“hana-0001”</span>，第二台云服务器为&nbsp;<span class="parmvalue" id="parmvalue918631614349"><a name="parmvalue918631614349"></a><a name="parmvalue918631614349"></a>“hana-0002”</span>，以此类推。</p>
    <p id="p11186171683416"><a name="p11186171683416"></a><a name="p11186171683416"></a>关于主机名的长度和字符的更多信息，参见SAP Note 611361。</p>
    </td>
    </tr>
    <tr id="row6531825193113"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p55319253315"><a name="p55319253315"></a><a name="p55319253315"></a>登录凭证</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p165392593117"><a name="p165392593117"></a><a name="p165392593117"></a>选择<span class="uicontrol" id="uicontrol9631124543110"><a name="uicontrol9631124543110"></a><a name="uicontrol9631124543110"></a>“密钥对”</span>。</p>
    </td>
    </tr>
    <tr id="row11182111616344"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p17182121610343"><a name="p17182121610343"></a><a name="p17182121610343"></a>密钥对</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p12183171643415"><a name="p12183171643415"></a><a name="p12183171643415"></a>仅在<span class="parmname" id="parmname14183121653415"><a name="parmname14183121653415"></a><a name="parmname14183121653415"></a>“登录凭证”</span>为<span class="parmvalue" id="parmvalue5183181619343"><a name="parmvalue5183181619343"></a><a name="parmvalue5183181619343"></a>“密钥对”</span>时生效。</p>
    <p id="p16183171612346"><a name="p16183171612346"></a><a name="p16183171612346"></a>指使用SSH密钥证书作为HANA云服务器的鉴权方式。请先单击<span class="uicontrol" id="uicontrol518351643412"><a name="uicontrol518351643412"></a><a name="uicontrol518351643412"></a>“新建密钥对”</span>，在<span class="wintitle" id="wintitle41831916133413"><a name="wintitle41831916133413"></a><a name="wintitle41831916133413"></a>“密钥对”</span>页面创建密钥。</p>
    <p id="p20183141616345"><a name="p20183141616345"></a><a name="p20183141616345"></a>需要指出的是，SAP HANA、SAP HANA Studio和NAT Server所使用的云服务器，必须指定同一份密钥，否则会导致后续SAP HANA无法正常安装。</p>
    <div class="note" id="note1518391663420"><a name="note1518391663420"></a><a name="note1518391663420"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p19183141613419"><a name="p19183141613419"></a><a name="p19183141613419"></a>如果您直接从下拉列表中选择已有的SSH密钥证书，请确保您已在本地获取该文件，否则，将影响您正常登录HANA云服务器。</p>
    <p id="p1418361633413"><a name="p1418361633413"></a><a name="p1418361633413"></a>若需要创建密钥，则其创建方法为：</p>
    <p id="p1818351673410"><a name="p1818351673410"></a><a name="p1818351673410"></a>单击<span class="uicontrol" id="uicontrol1118314168349"><a name="uicontrol1118314168349"></a><a name="uicontrol1118314168349"></a>“新建密钥对”</span>后，在弹出的界面中单击<span class="uicontrol" id="uicontrol3183131616344"><a name="uicontrol3183131616344"></a><a name="uicontrol3183131616344"></a>“创建密钥对”</span>，输入密钥名称后单击<span class="uicontrol" id="uicontrol7183151617340"><a name="uicontrol7183151617340"></a><a name="uicontrol7183151617340"></a>“确定”</span>，并在系统弹出的提示框中单击<span class="uicontrol" id="uicontrol1183101612345"><a name="uicontrol1183101612345"></a><a name="uicontrol1183101612345"></a>“确定”</span>，然后根据提示信息查看并保存私钥即可。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row18749124602618"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p2750046182612"><a name="p2750046182612"></a><a name="p2750046182612"></a>云备份</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1890061014292"><a name="p1890061014292"></a><a name="p1890061014292"></a>云备份提供对云硬盘和弹性云服务器的备份保护，并支持利用备份数据恢复云服务器和云硬盘的数据。云备份设置完成后，系统会将弹性云服务器绑定至云备份存储库并绑定所选备份策略，定期备份弹性云服务器。</p>
    <p id="p9900410122917"><a name="p9900410122917"></a><a name="p9900410122917"></a>您可以根据实际情况选择以下三种方式。</p>
    <a name="ul4616427112912"></a><a name="ul4616427112912"></a><ul id="ul4616427112912"><li>现在购买：<a name="ol17616132712290"></a><a name="ol17616132712290"></a><ol id="ol17616132712290"><li>输入云备份存储库的名称：只能由中文字符、英文字母、数字、下划线、中划线组成，且长度小于等于64个字符。例如：vault-f61e。默认的命名规则为“vault_xxxx”。</li><li>输入存储库的容量：此容量为备份云服务器所需的容量。存储库的空间不能小于云服务器的空间。取值范围为[云服务器总容量，10485760]GB。</li><li>设置备份策略：在下拉列表中选择备份策略，或进入云备份控制台查看或编辑备份策略。</li></ol>
    </li><li>使用已有：<a name="ol2061632722913"></a><a name="ol2061632722913"></a><ol id="ol2061632722913"><li>选择云备份存储库的：在下拉列表中选择已有的云备份存储库。</li><li>设置备份策略：在下拉列表中选择备份策略，或进入云备份控制台查看或编辑备份策略。</li></ol>
    </li><li>暂不购买：跳过云备份的配置步骤。如云服务器购买成功后仍需设置备份保护，请进入云备份控制台找到目标存储库，绑定服务器。</li></ul>
    </td>
    </tr>
    <tr id="row17184171683411"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1118441673420"><a name="p1118441673420"></a><a name="p1118441673420"></a>云服务器组</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p61848160341"><a name="p61848160341"></a><a name="p61848160341"></a>用于指定HANA云服务器的服务器组。系统在创建云服务器时，会将属于同一个服务器组的HANA云服务器，创建在不同的物理主机上，以保证HANA云服务器运行的可靠性。</p>
    <p id="p6184101619343"><a name="p6184101619343"></a><a name="p6184101619343"></a>因此，需要根据具体的场景来确定策略：</p>
    <a name="ul1618431614345"></a><a name="ul1618431614345"></a><ul id="ul1618431614345"><li>单节点无HA：不需要指定<span class="parmvalue" id="parmvalue14184161643415"><a name="parmvalue14184161643415"></a><a name="parmvalue14184161643415"></a>“云服务器组”</span>。</li><li>单节点HA：两台HANA云服务器必须属于同一个<span class="parmvalue" id="parmvalue8185151619341"><a name="parmvalue8185151619341"></a><a name="parmvalue8185151619341"></a>“云服务器组”</span>。</li></ul>
    <div class="note" id="note1718520162345"><a name="note1718520162345"></a><a name="note1718520162345"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p121851816173413"><a name="p121851816173413"></a><a name="p121851816173413"></a>如果还没有云服务器组，则其创建方法为：</p>
    <p id="p19185116133411"><a name="p19185116133411"></a><a name="p19185116133411"></a>单击<span class="uicontrol" id="uicontrol1318551619348"><a name="uicontrol1318551619348"></a><a name="uicontrol1318551619348"></a>“新建云服务器组”</span>，在弹出的界面上，单击<span class="uicontrol" id="uicontrol418511616345"><a name="uicontrol418511616345"></a><a name="uicontrol418511616345"></a>“创建云服务器组”</span>，输入云服务器组名称后单击<span class="uicontrol" id="uicontrol91857161343"><a name="uicontrol91857161343"></a><a name="uicontrol91857161343"></a>“确定”</span>即可。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row1119015114311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p25001810163214"><a name="p25001810163214"></a><a name="p25001810163214"></a>高级选项</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p6500181013210"><a name="p6500181013210"></a><a name="p6500181013210"></a>选择<span class="uicontrol" id="uicontrol17132430123216"><a name="uicontrol17132430123216"></a><a name="uicontrol17132430123216"></a>“现在配置”</span>。</p>
    </td>
    </tr>
    <tr id="row17185141653416"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p14185116133418"><a name="p14185116133418"></a><a name="p14185116133418"></a>委托</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p18185191683410"><a name="p18185191683410"></a><a name="p18185191683410"></a>此参数需要勾选<span class="parmname" id="parmname91851416173420"><a name="parmname91851416173420"></a><a name="parmname91851416173420"></a>“高级选项”</span>后面的<span class="uicontrol" id="uicontrol15185191623411"><a name="uicontrol15185191623411"></a><a name="uicontrol15185191623411"></a>“现在配置”</span>，展开页面后才能看到。</p>
    <p id="p13185916173410"><a name="p13185916173410"></a><a name="p13185916173410"></a>选择代理后可以使被委托方通过该代理获取临时访问公有云的凭据。</p>
    <p id="p16185316133414"><a name="p16185316133414"></a><a name="p16185316133414"></a>Data Provider是公有云平台的指标收集器，用于收集SAP NetWeaver系统中ECS和CES的关键性能数据并将其呈现给SAP应用。当SAP HANA与SAP NetWeaver共同部署时，需要指定<span class="parmvalue" id="parmvalue1918510162349"><a name="parmvalue1918510162349"></a><a name="parmvalue1918510162349"></a>“DataproviderAccess”</span>代理。</p>
    <p id="p1618551615349"><a name="p1618551615349"></a><a name="p1618551615349"></a>需要先以租户管理员的身份登录公有云管理控制台后，创建名为<span class="parmvalue" id="parmvalue161851016163419"><a name="parmvalue161851016163419"></a><a name="parmvalue161851016163419"></a>“DataproviderAccess”</span>的代理后，再在此处使用该代理。</p>
    <p id="p18959191815349"><a name="p18959191815349"></a><a name="p18959191815349"></a>新建委托具体操作请参见<a href="https://support.huaweicloud.com/dpug-sap/sap_01_0004.html" target="_blank" rel="noopener noreferrer">《Data Provider用户指南》</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

10. 单击“下一步：确认配置”。
11. 根据界面提示，确认HANA云服务器配置信息，如[表4](#table127431131614)所示。

    **表 4**  HANA云服务器配置信息

    <a name="table127431131614"></a>
    <table><thead align="left"><tr id="row47441413767"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p1674417130611"><a name="p1674417130611"></a><a name="p1674417130611"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p1074411318614"><a name="p1074411318614"></a><a name="p1074411318614"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row774519138616"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p19745131314618"><a name="p19745131314618"></a><a name="p19745131314618"></a>企业项目</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p15745141317616"><a name="p15745141317616"></a><a name="p15745141317616"></a>选择已创建的企业项目名称，例如：SAP。</p>
    </td>
    </tr>
    <tr id="row4917744597"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p75611059998"><a name="p75611059998"></a><a name="p75611059998"></a>购买时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1556110591096"><a name="p1556110591096"></a><a name="p1556110591096"></a>根据实际需要选择购买时长。</p>
    </td>
    </tr>
    <tr id="row07471113860"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p12561155913915"><a name="p12561155913915"></a><a name="p12561155913915"></a>购买数量</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p75611597912"><a name="p75611597912"></a><a name="p75611597912"></a>根据实际填写。</p>
    </td>
    </tr>
    <tr id="row18812421675"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p58601590496"><a name="p58601590496"></a><a name="p58601590496"></a>协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p198601974918"><a name="p198601974918"></a><a name="p198601974918"></a>勾选“我已经阅读并同意《华为镜像免责声明》”。</p>
    </td>
    </tr>
    </tbody>
    </table>

12. 单击“立即购买“，根据界面提示购买。
13. 购买完成后，系统返回“弹性云服务器“管理界面，可在右侧界面的“任务状态“后面，查看当前创建任务的状态。

    HANA云服务器创建完成后，在右侧界面的服务器列表中可查看到对应的服务器。

14. 根据需要，继续创建其他HANA云服务器。
15. 修改所有HANA云服务器的“root“帐号密码。

    “root“帐号密码非常重要，请务必牢记密码。同时请确保所有的HANA云服务器，“root“帐号密码保持一致。

    1.  通过密钥，登录到SAP HANA云服务器。
    2.  修改“root“帐号密码。

        **passwd**

        按照界面提示，输入密码并进行确认。



