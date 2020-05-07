# 创建VPC<a name="saphana_02_0019"></a>

SAP HANA系统的所有服务器都在同一个VPC中，需要为SAP  HANA申请VPC，并指定VPC中的子网网段。

## 操作步骤<a name="section5117508820456"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)，选择区域和项目。
3.  在左侧导航栏，单击![](figures/002.png)，选择“网络 \> 虚拟私有云“。
4.  在右侧界面，单击“创建虚拟私有云“，弹出“创建虚拟私有云“界面。
5.  在界面上，请参见[表1](#table65603559163645)配置VPC参数。

    **表 1**  虚拟私有云参数说明

    <a name="table65603559163645"></a>
    <table><thead align="left"><tr id="row30734839163645"><th class="cellrowborder" valign="top" width="15.229999999999999%" id="mcps1.2.5.1.1"><p id="p2189715415299"><a name="p2189715415299"></a><a name="p2189715415299"></a>分类</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.36%" id="mcps1.2.5.1.2"><p id="p36524908163645"><a name="p36524908163645"></a><a name="p36524908163645"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="36.75%" id="mcps1.2.5.1.3"><p id="p5727553163645"><a name="p5727553163645"></a><a name="p5727553163645"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="28.660000000000004%" id="mcps1.2.5.1.4"><p id="p61278663163645"><a name="p61278663163645"></a><a name="p61278663163645"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row14637060163645"><td class="cellrowborder" rowspan="5" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.1 "><p id="p2883902715299"><a name="p2883902715299"></a><a name="p2883902715299"></a>基本信息</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.36%" headers="mcps1.2.5.1.2 "><p id="p967724163645"><a name="p967724163645"></a><a name="p967724163645"></a>区域</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.75%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0070706438_p71311426132720"><a name="zh-cn_topic_0070706438_p71311426132720"></a><a name="zh-cn_topic_0070706438_p71311426132720"></a>区域指虚拟私有云所在的物理位置。同一区域内可用分区间内网互通，不同区域间内网不互通。可以在管理控制台左上角切换区域。</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.660000000000004%" headers="mcps1.2.5.1.4 "><p id="p41004165163645"><a name="p41004165163645"></a><a name="p41004165163645"></a>华北-北京四</p>
    </td>
    </tr>
    <tr id="row33493172163645"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p48204032163921"><a name="p48204032163921"></a><a name="p48204032163921"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p12212480163921"><a name="p12212480163921"></a><a name="p12212480163921"></a>VPC名称。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p49686796163921"><a name="p49686796163921"></a><a name="p49686796163921"></a>vpc-sap</p>
    </td>
    </tr>
    <tr id="row8101797163645"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p846641363818"><a name="p846641363818"></a><a name="p846641363818"></a>网段</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p13760765163947"><a name="p13760765163947"></a><a name="p13760765163947"></a>VPC的地址范围，VPC内的子网地址必须在VPC的地址范围内。</p>
    <p id="p56738021163947"><a name="p56738021163947"></a><a name="p56738021163947"></a>目前支持网段范围：</p>
    <p id="p40880148163947"><a name="p40880148163947"></a><a name="p40880148163947"></a>10.0.0.0/8~24</p>
    <p id="p32377018163947"><a name="p32377018163947"></a><a name="p32377018163947"></a>172.16.0.0/12~24</p>
    <p id="p22957712163947"><a name="p22957712163947"></a><a name="p22957712163947"></a>192.168.0.0/16~24</p>
    <p id="p04481525141216"><a name="p04481525141216"></a><a name="p04481525141216"></a>需要根据<a href="网络信息规划.md">网络信息规划</a>的子网信息，配置VPC的地址范围</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p47635417163947"><a name="p47635417163947"></a><a name="p47635417163947"></a>10.0.0.0/8</p>
    </td>
    </tr>
    <tr id="row1297310612317"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p5974106132318"><a name="p5974106132318"></a><a name="p5974106132318"></a>企业项目</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p11176521192310"><a name="p11176521192310"></a><a name="p11176521192310"></a>创建VPC时，可以将VPC加入已启用的企业项目。</p>
    <p id="p1017612118230"><a name="p1017612118230"></a><a name="p1017612118230"></a>企业项目管理提供了一种按企业项目管理云资源的方式，帮助您实现以企业项目为基本单元的资源及人员的统一管理，默认项目为default。</p>
    <p id="p101761721122314"><a name="p101761721122314"></a><a name="p101761721122314"></a>关于创建和管理企业项目的详情，请参见<a href="https://support.huaweicloud.com/usermanual-em/zh-cn_topic_0131965280.html" target="_blank" rel="noopener noreferrer">《企业管理用户指南》</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p19743617230"><a name="p19743617230"></a><a name="p19743617230"></a>SAP</p>
    </td>
    </tr>
    <tr id="row58854232152946"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p22171238152946"><a name="p22171238152946"></a><a name="p22171238152946"></a>标签</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p5594830615318"><a name="p5594830615318"></a><a name="p5594830615318"></a>虚拟私有云的标识，包括键和值。可以为虚拟私有云创建10个标签，此处为可选项，单击“高级配置”进行配置。</p>
    <p id="p3377270815318"><a name="p3377270815318"></a><a name="p3377270815318"></a>标签的命名规则请参考<a href="https://support.huaweicloud.com/usermanual-vpc/zh-cn_topic_0013935842.html#zh-cn_topic_0013935842__table63360804153019" target="_blank" rel="noopener noreferrer">虚拟私有云标签命名规则</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><a name="ul5846061515318"></a><a name="ul5846061515318"></a><ul id="ul5846061515318"><li>键：vpc_key1</li><li>值：vpc-01</li></ul>
    </td>
    </tr>
    <tr id="row43251058163645"><td class="cellrowborder" rowspan="8" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.1 "><p id="p15328238171724"><a name="p15328238171724"></a><a name="p15328238171724"></a>默认子网</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.36%" headers="mcps1.2.5.1.2 "><p id="p279310315257"><a name="p279310315257"></a><a name="p279310315257"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.75%" headers="mcps1.2.5.1.3 "><p id="p1779117352511"><a name="p1779117352511"></a><a name="p1779117352511"></a>可用区是指在同一地域内，电力和网络互相独立的物理区域。在同一VPC网络内可用区与可用区之间内网互通，可用区之间能做到物理隔离。</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.660000000000004%" headers="mcps1.2.5.1.4 "><p id="p1978913316253"><a name="p1978913316253"></a><a name="p1978913316253"></a>可用区1</p>
    </td>
    </tr>
    <tr id="row2058504212247"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p38801420164127"><a name="p38801420164127"></a><a name="p38801420164127"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p55907343164127"><a name="p55907343164127"></a><a name="p55907343164127"></a>子网的名称。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p32200914164127"><a name="p32200914164127"></a><a name="p32200914164127"></a>sap_Subnet</p>
    </td>
    </tr>
    <tr id="row29663353163645"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p53472873164127"><a name="p53472873164127"></a><a name="p53472873164127"></a>子网网段</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p36335493164127"><a name="p36335493164127"></a><a name="p36335493164127"></a>子网的地址范围，需要在VPC的地址范围内。需要根据<a href="网络信息规划.md">网络信息规划</a>的子网信息，配置子网网段。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p57493788164127"><a name="p57493788164127"></a><a name="p57493788164127"></a>10.0.3.0/24</p>
    </td>
    </tr>
    <tr id="row17539102592516"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1353942572518"><a name="p1353942572518"></a><a name="p1353942572518"></a>高级配置</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p155392025132516"><a name="p155392025132516"></a><a name="p155392025132516"></a>单击“高级配置”，可配置子网的高级参数，包括网关、DNS服务器地址等。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p185391254259"><a name="p185391254259"></a><a name="p185391254259"></a>默认配置</p>
    </td>
    </tr>
    <tr id="row60737684163645"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p153456716426"><a name="p153456716426"></a><a name="p153456716426"></a>网关</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p5719113516426"><a name="p5719113516426"></a><a name="p5719113516426"></a>子网的网关。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p197034316426"><a name="p197034316426"></a><a name="p197034316426"></a>10.0.0.1</p>
    </td>
    </tr>
    <tr id="row38289007164147"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p9056746164147"><a name="p9056746164147"></a><a name="p9056746164147"></a>DNS服务器地址</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p45170898164255"><a name="p45170898164255"></a><a name="p45170898164255"></a>默认情况下使用网络外部DNS服务器地址，如果需要修改DNS服务器地址，请确保配置的DNS服务器地址可用。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p29970286164147"><a name="p29970286164147"></a><a name="p29970286164147"></a>-</p>
    </td>
    </tr>
    <tr id="row227219701317"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p2027417711133"><a name="p2027417711133"></a><a name="p2027417711133"></a>DHCP租约时间</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p4493112191318"><a name="p4493112191318"></a><a name="p4493112191318"></a>DHCP租约时间是指DHCP服务器自动分配给客户端的IP地址的使用期限。超过租约时间，IP地址将被收回，需要重新分配。单位：天。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p11274873133"><a name="p11274873133"></a><a name="p11274873133"></a>365</p>
    </td>
    </tr>
    <tr id="row51723343153346"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p17332494154140"><a name="p17332494154140"></a><a name="p17332494154140"></a>标签</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p61754770154140"><a name="p61754770154140"></a><a name="p61754770154140"></a>子网的标识，包括键和值。可以为子网创建10个标签，此处为可选项。</p>
    <p id="p18922025154140"><a name="p18922025154140"></a><a name="p18922025154140"></a>标签的命名规则请参考<a href="https://support.huaweicloud.com/usermanual-vpc/zh-cn_topic_0013935842.html#zh-cn_topic_0013935842__table4168255153519" target="_blank" rel="noopener noreferrer">子网标签命名规则</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><a name="ul36839653154140"></a><a name="ul36839653154140"></a><ul id="ul36839653154140"><li>键：subnet_key1</li><li>值：subnet-01</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“立即创建“，完成VPC的创建。

