# 创建SFS<a name="saphana_02_0075"></a>

在SAP HANA系统中，Backup卷由SFS或SFS Turbo提供时，您可根据实际需要创建一个SFS或SFS Turbo，提供共享路径给SAP  HANA节点。

>![](public_sys-resources/icon-note.gif) **说明：**   
>**SFS与SFS Turbo的区别**  
>-   SFS是高带宽、大容量的文件存储服务，而SFS Turbo是低时延、高IOPS的文件存储服务。  
>-   SFS同时支持NFS和CIFS两种协议，SFS Turbo暂时仅支持NFS协议。  
>-   SFS Turbo相比SFS，更适用于企业OA类和高IOPS的业务场景。例如：高性能网站、在线日志打印、DevOps、压缩解压、容器应用和企业办公等。SFS更适用于HPC、媒体处理、文件共享和线下文件备份等大容量共享文件的场景。  
>-   功能上，SFS支持文件系统加密、支持使用多个VPC；SFS Turbo支持备份、文件系统加密和消息通知的功能。  

## 创建SFS<a name="section159371223279"></a>

1.  **（可选）购买SFS资源包**

    在SAP HANA系统中，创建SFS之前，您可根据实际需求购买SFS资源包。

    -   包年包月计费方式：可以购买包年包月套餐，提前规划资源的使用额度和时长。购买的资源包在生效期内，扣费方式是先扣除已购买的资源包内的额度后，超出部分以按量付费的方式进行结算。
    -   按需计费方式：如果您选择此种方式，可执行[2](#li1591745141713)创建SFS。

    1.  登录管理控制台。
    2.  在管理控制台左上角单击![](figures/icon-region-3.png)，选择区域和项目。
    3.  在左侧导航栏，单击![](figures/002-4.png)，选择“存储 \> 弹性文件服务“，进入“弹性文件服务”管理界面。
    4.  在右侧界面中，单击“购买SFS资源包”，系统弹出创建文件系统的界面。
    5.  在购买页面选择相关配置，具体请参见[表1](#table9978194425210)所示。

        **表 1**  配置参数说明

        <a name="table9978194425210"></a>
        <table><thead align="left"><tr id="row1097864417528"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p9978204415213"><a name="p9978204415213"></a><a name="p9978204415213"></a>名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p19781144175212"><a name="p19781144175212"></a><a name="p19781144175212"></a>说明</p>
        </th>
        <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p109786446529"><a name="p109786446529"></a><a name="p109786446529"></a>示例</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row15978544165211"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p139791744155214"><a name="p139791744155214"></a><a name="p139791744155214"></a>区域</p>
        </td>
        <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1236552305514"><a name="p1236552305514"></a><a name="p1236552305514"></a>不同的地域之间资源包不互通，每个地域需分别购买，请根据您的实际需求选择。</p>
        </td>
        <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1597994415210"><a name="p1597994415210"></a><a name="p1597994415210"></a>华北-北京四</p>
        </td>
        </tr>
        <tr id="row79799440523"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p99791444145220"><a name="p99791444145220"></a><a name="p99791444145220"></a>资源包规格</p>
        </td>
        <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p997916442523"><a name="p997916442523"></a><a name="p997916442523"></a>请根据实际需求选择资源包大小。</p>
        </td>
        <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1697964495216"><a name="p1697964495216"></a><a name="p1697964495216"></a>5TB</p>
        </td>
        </tr>
        <tr id="row5979344175216"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p29791944155219"><a name="p29791944155219"></a><a name="p29791944155219"></a>购买时长</p>
        </td>
        <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1497914465211"><a name="p1497914465211"></a><a name="p1497914465211"></a>请根据实际需求选择资源包生效时间。</p>
        </td>
        <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p997934435214"><a name="p997934435214"></a><a name="p997934435214"></a>1年</p>
        </td>
        </tr>
        </tbody>
        </table>

    6.  单击“立即购买”。
    7.  根据界面提示进行订单支付。

2.  <a name="li1591745141713"></a>创建SFS。
    1.  登录管理控制台。
    2.  在管理控制台左上角单击![](figures/icon-region-5.png)，选择区域和项目。
    3.  在左侧导航栏，单击![](figures/002-6.png)，选择“存储 \> 弹性文件服务“，进入“弹性文件服务”管理界面。
    4.  在右侧界面中，单击“创建文件系统”，系统弹出创建文件系统的界面。
    5.  输入参数信息，如[表2](#table14401713165211)所示。

        **表 2**  配置参数说明

        <a name="table14401713165211"></a>
        <table><thead align="left"><tr id="row19543171335217"><th class="cellrowborder" valign="top" width="19.919999999999998%" id="mcps1.2.4.1.1"><p id="p1054361305217"><a name="p1054361305217"></a><a name="p1054361305217"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="51.99%" id="mcps1.2.4.1.2"><p id="p95431813195218"><a name="p95431813195218"></a><a name="p95431813195218"></a>说明</p>
        </th>
        <th class="cellrowborder" valign="top" width="28.09%" id="mcps1.2.4.1.3"><p id="p53188413153"><a name="p53188413153"></a><a name="p53188413153"></a>示例</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row3924890915417"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p2504505115417"><a name="p2504505115417"></a><a name="p2504505115417"></a>文件系统类型</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p1538325415417"><a name="p1538325415417"></a><a name="p1538325415417"></a>文件系统类型，选择“SFS”。</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p331894121514"><a name="p331894121514"></a><a name="p331894121514"></a>SFS</p>
        </td>
        </tr>
        <tr id="row5424273125"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p17436274129"><a name="p17436274129"></a><a name="p17436274129"></a>区域</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p1943327101211"><a name="p1943327101211"></a><a name="p1943327101211"></a>请根据实际选择区域.</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p15640754191212"><a name="p15640754191212"></a><a name="p15640754191212"></a>华北-北京四</p>
        </td>
        </tr>
        <tr id="row1454331315215"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p2543121385217"><a name="p2543121385217"></a><a name="p2543121385217"></a>可用区</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p85431513185212"><a name="p85431513185212"></a><a name="p85431513185212"></a>指定文件服务所在的可用分区，请根据实际需要选择。</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p1431854191511"><a name="p1431854191511"></a><a name="p1431854191511"></a>可用区1</p>
        </td>
        </tr>
        <tr id="row4543191315213"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p9543131335216"><a name="p9543131335216"></a><a name="p9543131335216"></a>协议类型</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p1354316137526"><a name="p1354316137526"></a><a name="p1354316137526"></a>协议类型，选择“NFS”。</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p4318041101515"><a name="p4318041101515"></a><a name="p4318041101515"></a>NFS</p>
        </td>
        </tr>
        <tr id="row1754361325210"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p14543161395217"><a name="p14543161395217"></a><a name="p14543161395217"></a>虚拟私有云</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p55431913165220"><a name="p55431913165220"></a><a name="p55431913165220"></a>请选择SAP HANA对应的虚拟私有云。</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p5318144115157"><a name="p5318144115157"></a><a name="p5318144115157"></a>-</p>
        </td>
        </tr>
        <tr id="row117458359478"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p13747143534714"><a name="p13747143534714"></a><a name="p13747143534714"></a>自动扩容</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p374715353471"><a name="p374715353471"></a><a name="p374715353471"></a>默认开启自动扩容，开启自动扩容后，文件系统无容量限制，无需对容量进行调整。您可根据实际需求选择是否开启自动扩容。</p>
        <div class="notice" id="note18983324115518"><a name="note18983324115518"></a><a name="note18983324115518"></a><span class="noticetitle"> 须知： </span><div class="noticebody"><p id="p1298432413559"><a name="p1298432413559"></a><a name="p1298432413559"></a>若您已购买SFS资源包，则扣费方式如下：在已购买资源包的生效期内，扣费方式为先扣除已购买的资源包内的额度后，超出部分以按量付费的方式进行结算。</p>
        </div></div>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p0747113514719"><a name="p0747113514719"></a><a name="p0747113514719"></a>-</p>
        </td>
        </tr>
        <tr id="row054381315214"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p8543131313523"><a name="p8543131313523"></a><a name="p8543131313523"></a>最大容量</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p654351375210"><a name="p654351375210"></a><a name="p654351375210"></a>在关闭<span class="uicontrol" id="uicontrol968211616589"><a name="uicontrol968211616589"></a><a name="uicontrol968211616589"></a>“自动扩容”</span>后出现。单个文件系统的最大容量，具体要求请参见<a href="SAP-HANA节点规划.md">SAP HANA节点规划</a>的说明。</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p431884116155"><a name="p431884116155"></a><a name="p431884116155"></a>-</p>
        </td>
        </tr>
        <tr id="row886615241555"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p938211720514"><a name="p938211720514"></a><a name="p938211720514"></a>加密</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p038210717512"><a name="p038210717512"></a><a name="p038210717512"></a>可选参数。</p>
        <p id="p33828775116"><a name="p33828775116"></a><a name="p33828775116"></a>加密针对文件系统加密。可以新创建加密或者不加密的文件系统，无法更改已有文件系统的加密属性。如果设置文件系统加密，则勾选“加密”，具体配置可参见<a href="https://support.huaweicloud.com/qs-sfs/zh-cn_topic_0034428727.html" target="_blank" rel="noopener noreferrer">《弹性文件服务快速入门》</a>。</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p1876857145016"><a name="p1876857145016"></a><a name="p1876857145016"></a>-</p>
        </td>
        </tr>
        <tr id="row7611131016323"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p13505121812"><a name="p13505121812"></a><a name="p13505121812"></a>企业项目</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p150131161818"><a name="p150131161818"></a><a name="p150131161818"></a>请根据实际选择所在项目。</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p205013111182"><a name="p205013111182"></a><a name="p205013111182"></a>SAP</p>
        </td>
        </tr>
        <tr id="row1543111311524"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p1771653713324"><a name="p1771653713324"></a><a name="p1771653713324"></a>名称</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p1471583714322"><a name="p1471583714322"></a><a name="p1471583714322"></a>文件系统名称。</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p1713437183214"><a name="p1713437183214"></a><a name="p1713437183214"></a>sfs-share-001</p>
        </td>
        </tr>
        <tr id="row650110180"><td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.4.1.1 "><p id="p754371315528"><a name="p754371315528"></a><a name="p754371315528"></a>购买量</p>
        </td>
        <td class="cellrowborder" valign="top" width="51.99%" headers="mcps1.2.4.1.2 "><p id="p115431013145215"><a name="p115431013145215"></a><a name="p115431013145215"></a>请根据实际选择购买数量。</p>
        </td>
        <td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.3 "><p id="p1318441101510"><a name="p1318441101510"></a><a name="p1318441101510"></a>1</p>
        </td>
        </tr>
        </tbody>
        </table>

    6.  单击“立即创建“，在弹出的页面确认配置信息后，单击“提交”，等待任务创建成功，完成文件系统创建。
    7.  返回“弹性文件服务”管理界面，根据文件系统名称找到已创建的文件系统，并在“共享路径”栏查询共享路径。
    8.  登录SAP HANA节点查看“/etc/resolv.conf”文件是否配置DNS服务器的IP地址，如未配置需将DNS服务器的IP地址写入“/etc/resolv.conf”文件。


## 创建SFS Turbo<a name="section1078014199295"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region-7.png)，选择区域和项目。
3.  在左侧导航栏，单击![](figures/002-8.png)，选择“存储 \> 弹性文件服务“，进入“弹性文件服务”管理界面。
4.  在右侧界面中，单击“创建文件系统”，系统弹出创建文件系统的界面。
5.  输入参数信息，如[表3](#table47208541602)所示。

    **表 3**  配置参数说明

    <a name="table47208541602"></a>
    <table><thead align="left"><tr id="row1272075415013"><th class="cellrowborder" valign="top" width="19.42%" id="mcps1.2.4.1.1"><p id="p272017544013"><a name="p272017544013"></a><a name="p272017544013"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="55.379999999999995%" id="mcps1.2.4.1.2"><p id="p137204547011"><a name="p137204547011"></a><a name="p137204547011"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.2%" id="mcps1.2.4.1.3"><p id="p29281650201913"><a name="p29281650201913"></a><a name="p29281650201913"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row77209541705"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p2720185414018"><a name="p2720185414018"></a><a name="p2720185414018"></a>文件系统类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p6720654407"><a name="p6720654407"></a><a name="p6720654407"></a>文件系统类型，选择“SFS Turbo”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p1928155041916"><a name="p1928155041916"></a><a name="p1928155041916"></a>SFS Turbo</p>
    </td>
    </tr>
    <tr id="row94341215154010"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p1628115351124"><a name="p1628115351124"></a><a name="p1628115351124"></a>计费模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p17282133511124"><a name="p17282133511124"></a><a name="p17282133511124"></a>请根据实际选择计费模式。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p13282335191218"><a name="p13282335191218"></a><a name="p13282335191218"></a>包年/包月</p>
    </td>
    </tr>
    <tr id="row165297325195"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p585994201910"><a name="p585994201910"></a><a name="p585994201910"></a>区域</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p585917425198"><a name="p585917425198"></a><a name="p585917425198"></a>根据实际选择区域.</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p195712212135"><a name="p195712212135"></a><a name="p195712212135"></a>华北-北京四</p>
    </td>
    </tr>
    <tr id="row185941653183819"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p12721145417012"><a name="p12721145417012"></a><a name="p12721145417012"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p1372117541108"><a name="p1372117541108"></a><a name="p1372117541108"></a>指定文件服务所在的可用分区，请根据实际需要选择。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p1492895071910"><a name="p1492895071910"></a><a name="p1492895071910"></a>可用区1</p>
    </td>
    </tr>
    <tr id="row1172085419013"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p1072119544010"><a name="p1072119544010"></a><a name="p1072119544010"></a>协议类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p1572117546014"><a name="p1572117546014"></a><a name="p1572117546014"></a>文件服务类型，选择“NFS”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p13928165015191"><a name="p13928165015191"></a><a name="p13928165015191"></a>NFS</p>
    </td>
    </tr>
    <tr id="row117212542020"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p7353131164218"><a name="p7353131164218"></a><a name="p7353131164218"></a>存储类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p1595711543361"><a name="p1595711543361"></a><a name="p1595711543361"></a>请根据需要选择存储类型。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p1035212111426"><a name="p1035212111426"></a><a name="p1035212111426"></a>标准型</p>
    </td>
    </tr>
    <tr id="row117211854803"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p93510118429"><a name="p93510118429"></a><a name="p93510118429"></a>容量</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p435151154213"><a name="p435151154213"></a><a name="p435151154213"></a>单个文件系统的最大容量，当文件系统的实际使用容量达到该值时，您将无法对文件系统执行写入操作，需要进行扩容。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p19339734111017"><a name="p19339734111017"></a><a name="p19339734111017"></a>5TB</p>
    </td>
    </tr>
    <tr id="row4994185152217"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p15615122103619"><a name="p15615122103619"></a><a name="p15615122103619"></a>选择网络</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p1050585018472"><a name="p1050585018472"></a><a name="p1050585018472"></a>请选择要使用的服务器对应的虚拟私有云和子网，具体请参见<a href="创建VPC.md">创建VPC</a>和<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p11994657225"><a name="p11994657225"></a><a name="p11994657225"></a>-</p>
    </td>
    </tr>
    <tr id="row872135415014"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p1824811308386"><a name="p1824811308386"></a><a name="p1824811308386"></a>安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p72481307384"><a name="p72481307384"></a><a name="p72481307384"></a>请选择要使用的服务器对应的安全组，具体请参见<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p192820507195"><a name="p192820507195"></a><a name="p192820507195"></a>-</p>
    </td>
    </tr>
    <tr id="row661215523502"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p185621516135111"><a name="p185621516135111"></a><a name="p185621516135111"></a>自动备份</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p1956212169518"><a name="p1956212169518"></a><a name="p1956212169518"></a>可选参数。</p>
    <p id="p175621162519"><a name="p175621162519"></a><a name="p175621162519"></a>SFS Turbo同时提供自动备份功能，可以通过设置备份策略对文件系统的数据进行备份。启用备份策略后，系统会在指定的时间自动备份文件系统数据。</p>
    <p id="p185628167518"><a name="p185628167518"></a><a name="p185628167518"></a>勾选<span class="uicontrol" id="uicontrol565493310361"><a name="uicontrol565493310361"></a><a name="uicontrol565493310361"></a>“使用自动备份”</span>。启用后则需要设置“备份开始时间”和“备份周期”，您可以使用根据业务需求创建备份策略。</p>
    <p id="p1562316145113"><a name="p1562316145113"></a><a name="p1562316145113"></a>具体参数请参见《弹性文件服务快速入门》中创建文件系统中的<a href="https://support.huaweicloud.com/qs-sfs/zh-cn_topic_0034428727.html#zh-cn_topic_0034428727__table13661412163911" target="_blank" rel="noopener noreferrer">表3</a>所示。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p1961245218507"><a name="p1961245218507"></a><a name="p1961245218507"></a>-</p>
    </td>
    </tr>
    <tr id="row43141950161518"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p145930238486"><a name="p145930238486"></a><a name="p145930238486"></a>企业项目</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p6765251134810"><a name="p6765251134810"></a><a name="p6765251134810"></a>请根据实际选择所在项目。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p1676585104811"><a name="p1676585104811"></a><a name="p1676585104811"></a>SAP</p>
    </td>
    </tr>
    <tr id="row59784474912"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p372110541505"><a name="p372110541505"></a><a name="p372110541505"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p1272116541506"><a name="p1272116541506"></a><a name="p1272116541506"></a>文件服务名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p18928450151910"><a name="p18928450151910"></a><a name="p18928450151910"></a>sfs-turbo-backup</p>
    </td>
    </tr>
    <tr id="row116931143141012"><td class="cellrowborder" valign="top" width="19.42%" headers="mcps1.2.4.1.1 "><p id="p149414294143"><a name="p149414294143"></a><a name="p149414294143"></a>购买量</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.379999999999995%" headers="mcps1.2.4.1.2 "><p id="p1294102961416"><a name="p1294102961416"></a><a name="p1294102961416"></a>请根据实际选择购买量。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.2%" headers="mcps1.2.4.1.3 "><p id="p159419299145"><a name="p159419299145"></a><a name="p159419299145"></a>1年</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“立即创建“，在弹出的页面确认配置信息后，单击“提交”，等待任务创建成功，完成文件系统创建。
7.  返回“弹性文件服务”管理界面，根据文件系统名称找到已创建的文件系统，并在“共享路径”栏查询共享路径。
8.  登录SAP HANA节点查看“/etc/resolv.conf”文件是否配置DNS服务器的IP地址，如未配置需将DNS服务器的IP地址写入“/etc/resolv.conf”文件。

