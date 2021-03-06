# 查询镜像详情（OpenStack原生）<a name="ZH-CN_TOPIC_0020091566"></a>

## 功能介绍<a name="section39958021"></a>

查询单个镜像详情，用户可以通过该接口查询单个私有或者公共镜像的详情。

## URI<a name="section24077873"></a>

-   URI格式

    GET /v2/images/\{image\_id\}

-   参数说明

    <a name="table37590215162351"></a>
    <table><thead align="left"><tr id="row14906674162351"><th class="cellrowborder" valign="top" width="30.82691730826917%" id="mcps1.1.5.1.1"><p id="p66589937162351"><a name="p66589937162351"></a><a name="p66589937162351"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.2979702029797%" id="mcps1.1.5.1.2"><p id="p25075841162351"><a name="p25075841162351"></a><a name="p25075841162351"></a>是否为必须</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.048195180481947%" id="mcps1.1.5.1.3"><p id="p3182134421246"><a name="p3182134421246"></a><a name="p3182134421246"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="30.82691730826917%" id="mcps1.1.5.1.4"><p id="p17877258162351"><a name="p17877258162351"></a><a name="p17877258162351"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row38771763162351"><td class="cellrowborder" valign="top" width="30.82691730826917%" headers="mcps1.1.5.1.1 "><p id="p53505060162351"><a name="p53505060162351"></a><a name="p53505060162351"></a>image_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.2979702029797%" headers="mcps1.1.5.1.2 "><p id="p38942598162351"><a name="p38942598162351"></a><a name="p38942598162351"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.048195180481947%" headers="mcps1.1.5.1.3 "><p id="p2739208421246"><a name="p2739208421246"></a><a name="p2739208421246"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.82691730826917%" headers="mcps1.1.5.1.4 "><p id="p233856162351"><a name="p233856162351"></a><a name="p233856162351"></a>镜像ID</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section15374270"></a>

请求样例

```
GET /v2/images/33ad552d-1149-471c-8190-ff6776174a00
```

## 响应<a name="section4150710"></a>

-   参数说明

    <a name="table3940930519484"></a>
    <table><thead align="left"><tr id="row5108650619484"><th class="cellrowborder" valign="top" width="36.9%" id="mcps1.1.4.1.1"><p id="p4436630719484"><a name="p4436630719484"></a><a name="p4436630719484"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.700000000000003%" id="mcps1.1.4.1.2"><p id="p3690111319484"><a name="p3690111319484"></a><a name="p3690111319484"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="36.4%" id="mcps1.1.4.1.3"><p id="p3620014719484"><a name="p3620014719484"></a><a name="p3620014719484"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row4653077719484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p1089662919484"><a name="p1089662919484"></a><a name="p1089662919484"></a>file</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p1021172419484"><a name="p1021172419484"></a><a name="p1021172419484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p2184333619484"><a name="p2184333619484"></a><a name="p2184333619484"></a>镜像文件下载和上传链接。</p>
    </td>
    </tr>
    <tr id="row6237230419484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p1899183819484"><a name="p1899183819484"></a><a name="p1899183819484"></a>owner</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p6194387619484"><a name="p6194387619484"></a><a name="p6194387619484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p5139805919484"><a name="p5139805919484"></a><a name="p5139805919484"></a>镜像属于哪个租户。</p>
    </td>
    </tr>
    <tr id="row5992935019484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p2243918519484"><a name="p2243918519484"></a><a name="p2243918519484"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p563467219484"><a name="p563467219484"></a><a name="p563467219484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p5375527619484"><a name="p5375527619484"></a><a name="p5375527619484"></a>镜像ID。</p>
    </td>
    </tr>
    <tr id="row1403543619484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p6312849319484"><a name="p6312849319484"></a><a name="p6312849319484"></a>size</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p1313430319484"><a name="p1313430319484"></a><a name="p1313430319484"></a>Long</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p5724560919484"><a name="p5724560919484"></a><a name="p5724560919484"></a>目前暂时不使用。</p>
    </td>
    </tr>
    <tr id="row4544843919484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p5744495319484"><a name="p5744495319484"></a><a name="p5744495319484"></a>self</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p2252964019484"><a name="p2252964019484"></a><a name="p2252964019484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p1296154719484"><a name="p1296154719484"></a><a name="p1296154719484"></a>镜像链接信息。</p>
    </td>
    </tr>
    <tr id="row4954506419484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p5372723719484"><a name="p5372723719484"></a><a name="p5372723719484"></a>schema</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p5693892219484"><a name="p5693892219484"></a><a name="p5693892219484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p4864998419484"><a name="p4864998419484"></a><a name="p4864998419484"></a>镜像视图。</p>
    </td>
    </tr>
    <tr id="row3519667719484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p3235856619484"><a name="p3235856619484"></a><a name="p3235856619484"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p379822119484"><a name="p379822119484"></a><a name="p379822119484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p32131061155224"><a name="p32131061155224"></a><a name="p32131061155224"></a>镜像状态。取值如下：</p>
    <a name="ul43292299155227"></a><a name="ul43292299155227"></a><ul id="ul43292299155227"><li>queued：表示镜像元数据已经创建成功，等待上传镜像文件。</li><li>saving：表示镜像正在上传文件到后端存储。</li><li>deleted：表示镜像已经删除。</li><li>killed：表示镜像上传错误。</li><li>active：表示镜像可以正常使用。</li></ul>
    </td>
    </tr>
    <tr id="row1743970919484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p333030119484"><a name="p333030119484"></a><a name="p333030119484"></a>tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p131897419484"><a name="p131897419484"></a><a name="p131897419484"></a>List&lt;String&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p3972807119484"><a name="p3972807119484"></a><a name="p3972807119484"></a>镜像标签列表，提供用户可以自定义管理私有镜像的能力。用户可以通过镜像标签接口为每个镜像增加不同的标签，在查询接口中可以根据标签进行过滤。</p>
    </td>
    </tr>
    <tr id="row2200832719484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p3784404819484"><a name="p3784404819484"></a><a name="p3784404819484"></a>visibility</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p4546904619484"><a name="p4546904619484"></a><a name="p4546904619484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p5911408019484"><a name="p5911408019484"></a><a name="p5911408019484"></a>是否被其他租户可见，取值为private或public。</p>
    </td>
    </tr>
    <tr id="row6226467419484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p1027383819484"><a name="p1027383819484"></a><a name="p1027383819484"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p2687454619484"><a name="p2687454619484"></a><a name="p2687454619484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p2935464719484"><a name="p2935464719484"></a><a name="p2935464719484"></a>镜像名称。name参数说明请参考<a href="镜像属性.md#section61598810155254">镜像属性</a>。</p>
    </td>
    </tr>
    <tr id="row6286523719484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p5891947019484"><a name="p5891947019484"></a><a name="p5891947019484"></a>checksum</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p774777119484"><a name="p774777119484"></a><a name="p774777119484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p2358973319484"><a name="p2358973319484"></a><a name="p2358973319484"></a>目前暂时不使用。</p>
    </td>
    </tr>
    <tr id="row1098100819484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p1704644719484"><a name="p1704644719484"></a><a name="p1704644719484"></a>deleted</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p3858499119484"><a name="p3858499119484"></a><a name="p3858499119484"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p3837658419484"><a name="p3837658419484"></a><a name="p3837658419484"></a>是否是删除的镜像，取值为true或者false。</p>
    </td>
    </tr>
    <tr id="row984493719484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p5924239319484"><a name="p5924239319484"></a><a name="p5924239319484"></a>protected</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p3390450119484"><a name="p3390450119484"></a><a name="p3390450119484"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p6191008619484"><a name="p6191008619484"></a><a name="p6191008619484"></a>是否是受保护的，受保护的镜像不允许删除。取值为true或false。</p>
    </td>
    </tr>
    <tr id="row2031987019484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p3529679319484"><a name="p3529679319484"></a><a name="p3529679319484"></a>container_format</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p4046799719484"><a name="p4046799719484"></a><a name="p4046799719484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p5668228819484"><a name="p5668228819484"></a><a name="p5668228819484"></a>容器类型。</p>
    </td>
    </tr>
    <tr id="row4037855219484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p4943728819484"><a name="p4943728819484"></a><a name="p4943728819484"></a>min_ram</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p4499737219484"><a name="p4499737219484"></a><a name="p4499737219484"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p2090850919484"><a name="p2090850919484"></a><a name="p2090850919484"></a>镜像运行最小内存，单位为MB。取值参考弹性云服务器规格限制，一般设置为0。</p>
    </td>
    </tr>
    <tr id="row5395885319484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p859097919484"><a name="p859097919484"></a><a name="p859097919484"></a>updated_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p2478073819484"><a name="p2478073819484"></a><a name="p2478073819484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p6108279419484"><a name="p6108279419484"></a><a name="p6108279419484"></a>更新时间。格式为UTC时间。</p>
    </td>
    </tr>
    <tr id="row1287423619484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p3618021119484"><a name="p3618021119484"></a><a name="p3618021119484"></a>__os_bit</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p4491600719484"><a name="p4491600719484"></a><a name="p4491600719484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p1431795119484"><a name="p1431795119484"></a><a name="p1431795119484"></a>操作系统位数，一般取值为“32”或者“64”。</p>
    </td>
    </tr>
    <tr id="row6175270019484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p3591283819484"><a name="p3591283819484"></a><a name="p3591283819484"></a>__os_version</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p2325879319484"><a name="p2325879319484"></a><a name="p2325879319484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p491406019484"><a name="p491406019484"></a><a name="p491406019484"></a>操作系统具体版本。</p>
    </td>
    </tr>
    <tr id="row4422654119484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p2558005119484"><a name="p2558005119484"></a><a name="p2558005119484"></a>__description</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p5871828719484"><a name="p5871828719484"></a><a name="p5871828719484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p5856077419484"><a name="p5856077419484"></a><a name="p5856077419484"></a>镜像描述信息。_description参数说明请参考<a href="镜像属性.md#section61598810155254">镜像属性</a>。</p>
    </td>
    </tr>
    <tr id="row5728492419484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p956729019484"><a name="p956729019484"></a><a name="p956729019484"></a>disk_format</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p3675300019484"><a name="p3675300019484"></a><a name="p3675300019484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p2420299019484"><a name="p2420299019484"></a><a name="p2420299019484"></a>镜像的格式，目前支持vhd，zvhd、raw，qcow2。默认值是vhd。</p>
    </td>
    </tr>
    <tr id="row1650032219484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p6145769619484"><a name="p6145769619484"></a><a name="p6145769619484"></a>__isregistered</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p1201748319484"><a name="p1201748319484"></a><a name="p1201748319484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p3389204219484"><a name="p3389204219484"></a><a name="p3389204219484"></a>是否是注册过的镜像，取值为“true”或者“false”。</p>
    </td>
    </tr>
    <tr id="row3659292519484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p1123691819484"><a name="p1123691819484"></a><a name="p1123691819484"></a>__platform</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p3777512719484"><a name="p3777512719484"></a><a name="p3777512719484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p3988644119484"><a name="p3988644119484"></a><a name="p3988644119484"></a>镜像平台分类，取值为Windows，Ubuntu，RedHat，SUSE，CentOS，Debian，OpenSUSE, Oracle Linux，Fedora，Other，CoreOS和EulerOS。</p>
    </td>
    </tr>
    <tr id="row2343365119484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p1907761719484"><a name="p1907761719484"></a><a name="p1907761719484"></a>__os_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p178315519484"><a name="p178315519484"></a><a name="p178315519484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p1021789019484"><a name="p1021789019484"></a><a name="p1021789019484"></a>操作系统类型，目前取值Linux， Windows，Other。</p>
    </td>
    </tr>
    <tr id="row2485214919484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p6686709019484"><a name="p6686709019484"></a><a name="p6686709019484"></a>min_disk</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p4752519919484"><a name="p4752519919484"></a><a name="p4752519919484"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p60826909104315"><a name="p60826909104315"></a><a name="p60826909104315"></a>镜像运行需要的最小磁盘容量，单位为GB 。取值为40～1024GB。</p>
    </td>
    </tr>
    <tr id="row1769644219484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p2412566319484"><a name="p2412566319484"></a><a name="p2412566319484"></a>virtual_env_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p802166419484"><a name="p802166419484"></a><a name="p802166419484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p4577507919484"><a name="p4577507919484"></a><a name="p4577507919484"></a>镜像使用环境类型：FusionCompute，Ironic，DataImage。如果弹性云服务器镜像，则取值为FusionCompute，如果是数据卷镜像则取值是DataImage，如果是裸金属服务器镜像，则取值是Ironic。</p>
    </td>
    </tr>
    <tr id="row932252719484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p1692720719484"><a name="p1692720719484"></a><a name="p1692720719484"></a>__image_source_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p2892650319484"><a name="p2892650319484"></a><a name="p2892650319484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p6134541619484"><a name="p6134541619484"></a><a name="p6134541619484"></a>镜像后端存储类型，目前只支持uds。</p>
    </td>
    </tr>
    <tr id="row1523783619484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p2630521719484"><a name="p2630521719484"></a><a name="p2630521719484"></a>__imagetype</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p5034781819484"><a name="p5034781819484"></a><a name="p5034781819484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p28701642133010"><a name="p28701642133010"></a><a name="p28701642133010"></a>镜像类型，目前支持以下类型：</p>
    <a name="ul387034210305"></a><a name="ul387034210305"></a><ul id="ul387034210305"><li>公共镜像：gold</li><li>私有镜像：private</li><li>共享镜像：shared</li></ul>
    </td>
    </tr>
    <tr id="row6211992119484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p6565767619484"><a name="p6565767619484"></a><a name="p6565767619484"></a>created_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p1667154419484"><a name="p1667154419484"></a><a name="p1667154419484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p821782019484"><a name="p821782019484"></a><a name="p821782019484"></a>创建时间。格式为UTC时间。</p>
    </td>
    </tr>
    <tr id="row685152319484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p1810251119484"><a name="p1810251119484"></a><a name="p1810251119484"></a>virtual_size</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p5701732019484"><a name="p5701732019484"></a><a name="p5701732019484"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p5500021319484"><a name="p5500021319484"></a><a name="p5500021319484"></a>目前暂时不使用。</p>
    </td>
    </tr>
    <tr id="row2523987519484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p3116399419484"><a name="p3116399419484"></a><a name="p3116399419484"></a>deleted_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p4125557719484"><a name="p4125557719484"></a><a name="p4125557719484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p5336746519484"><a name="p5336746519484"></a><a name="p5336746519484"></a>删除时间。格式为UTC时间。</p>
    </td>
    </tr>
    <tr id="row1054514319484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p4885024319484"><a name="p4885024319484"></a><a name="p4885024319484"></a>__originalimagename</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p6455557119484"><a name="p6455557119484"></a><a name="p6455557119484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p6161873519484"><a name="p6161873519484"></a><a name="p6161873519484"></a>父镜像ID。</p>
    <p id="p1769771019484"><a name="p1769771019484"></a><a name="p1769771019484"></a>公共镜像或通过文件创建的私有镜像，取值为空。</p>
    </td>
    </tr>
    <tr id="row2506166419484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p1672894219484"><a name="p1672894219484"></a><a name="p1672894219484"></a>__backup_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p1286707219484"><a name="p1286707219484"></a><a name="p1286707219484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p3559993519484"><a name="p3559993519484"></a><a name="p3559993519484"></a>备份ID。如果是备份创建的镜像，则填写为备份的ID，否则为空。</p>
    </td>
    </tr>
    <tr id="row5196396219484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p4833143119484"><a name="p4833143119484"></a><a name="p4833143119484"></a>__productcode</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p2253182819484"><a name="p2253182819484"></a><a name="p2253182819484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p1313876119484"><a name="p1313876119484"></a><a name="p1313876119484"></a>市场镜像的产品ID。</p>
    </td>
    </tr>
    <tr id="row5427752419484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p3440330819484"><a name="p3440330819484"></a><a name="p3440330819484"></a>__image_size</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p3520454019484"><a name="p3520454019484"></a><a name="p3520454019484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p3299550119484"><a name="p3299550119484"></a><a name="p3299550119484"></a>镜像文件的大小，单位为字节。目前取值为大于0的字符串。</p>
    </td>
    </tr>
    <tr id="row2852405719484"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p2874729419484"><a name="p2874729419484"></a><a name="p2874729419484"></a>__data_origin</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p4682946319484"><a name="p4682946319484"></a><a name="p4682946319484"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p3509015719484"><a name="p3509015719484"></a><a name="p3509015719484"></a>镜像来源。</p>
    <p id="p4737595819484"><a name="p4737595819484"></a><a name="p4737595819484"></a>公共镜像为空。</p>
    </td>
    </tr>
    <tr id="row55821842155911"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p25275315155911"><a name="p25275315155911"></a><a name="p25275315155911"></a>__sequence_num</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p5341551155911"><a name="p5341551155911"></a><a name="p5341551155911"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p30012506155911"><a name="p30012506155911"></a><a name="p30012506155911"></a>目前暂时不用</p>
    </td>
    </tr>
    <tr id="row59643047203735"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p580552184954"><a name="p580552184954"></a><a name="p580552184954"></a>__support_kvm</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p27540563184954"><a name="p27540563184954"></a><a name="p27540563184954"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p46304701184954"><a name="p46304701184954"></a><a name="p46304701184954"></a>如果镜像支持KVM，取值为true，否则无需增加该属性。</p>
    </td>
    </tr>
    <tr id="row3882825120219"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p23167082184954"><a name="p23167082184954"></a><a name="p23167082184954"></a>__support_xen</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p11995013184954"><a name="p11995013184954"></a><a name="p11995013184954"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p4154542184954"><a name="p4154542184954"></a><a name="p4154542184954"></a>如果镜像支持XEN，取值为true，否则无需增加该属性。</p>
    </td>
    </tr>
    <tr id="row43057536203728"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p47581434184954"><a name="p47581434184954"></a><a name="p47581434184954"></a>__support_diskintensive</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p50609959184954"><a name="p50609959184954"></a><a name="p50609959184954"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p20887878184954"><a name="p20887878184954"></a><a name="p20887878184954"></a>表示该镜像支持密集存储。如果镜像支持密集存储性能，则值为true，否则无需增加该属性。镜像操作系统类型请参考<a href="相关参数取值列表.md#table48545918250">表3</a>。</p>
    </td>
    </tr>
    <tr id="row39724815224743"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p17123543184954"><a name="p17123543184954"></a><a name="p17123543184954"></a>__support_highperformance</p>
    <p id="p65009787184954"><a name="p65009787184954"></a><a name="p65009787184954"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p38086855184954"><a name="p38086855184954"></a><a name="p38086855184954"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p17225863184954"><a name="p17225863184954"></a><a name="p17225863184954"></a>表示该镜像支持高计算性能。如果镜像支持高计算性能，则值为true，否则无需增加该属性。镜像操作系统类型请参考<a href="相关参数取值列表.md#table48545918250">表3</a>。</p>
    </td>
    </tr>
    <tr id="row62323042204110"><td class="cellrowborder" valign="top" width="36.9%" headers="mcps1.1.4.1.1 "><p id="p26024330184954"><a name="p26024330184954"></a><a name="p26024330184954"></a>__support_xen_gpu_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.700000000000003%" headers="mcps1.1.4.1.2 "><p id="p15739313184954"><a name="p15739313184954"></a><a name="p15739313184954"></a>String</p>
    <p id="p8538247184954"><a name="p8538247184954"></a><a name="p8538247184954"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="36.4%" headers="mcps1.1.4.1.3 "><p id="p23482902184954"><a name="p23482902184954"></a><a name="p23482902184954"></a>表示该镜像是支持XEN虚拟化平台下的GPU优化类型，取值参考<a href="相关参数取值列表.md#table65768383152758">表2</a>。镜像操作系统类型请参考<a href="相关参数取值列表.md#table48545918250">表3</a>。如果不支持XEN虚拟化下GPU类型，无需添加该属性。该属性与“__support_xen”和“__support_kvm”属性不共存。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    STATUS CODE 200
    ```

    ```
    {
          "schema": "/v2/schemas/image",
          "min_disk": 100,
          "created_at": "2018-09-06T14:03:27Z",
          "__image_source_type": "uds",
          "container_format": "bare",
          "file": "/v2/images/bc6bed6e-ba3a-4447-afcc-449174a3eb52/file",
          "updated_at": "2018-09-06T15:17:33Z",
          "protected": true,
          "checksum": "d41d8cd98f00b204e9800998ecf8427e",
          "__support_kvm_fpga_type": "VU9P",
          "id": "bc6bed6e-ba3a-4447-afcc-449174a3eb52",
          "__isregistered": "true",
          "min_ram": 2048,
          "__lazyloading": "true",
          "owner": "1bed856811654c1cb661a6ca845ebc77",
          "__os_type": "Linux",
          "__imagetype": "gold",
          "visibility": "public",
          "virtual_env_type": "FusionCompute",
          "tags": [],
          "__platform": "CentOS",
          "size": 0,
          "__os_bit": "64",
          "__os_version": "CentOS 7.3 64bit",
          "name": "CentOS 7.3 64bit vivado",
          "self": "/v2/images/bc6bed6e-ba3a-4447-afcc-449174a3eb52",
          "disk_format": "zvhd2",
          "virtual_size": null,
          "status": "active"
    }
    ```


## 返回值<a name="section37356392"></a>

-   正常

    200

-   异常

    <a name="table262968317230"></a>
    <table><thead align="left"><tr id="row5740081817230"><th class="cellrowborder" valign="top" width="46.54%" id="mcps1.1.3.1.1"><p id="p1895465817230"><a name="p1895465817230"></a><a name="p1895465817230"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.459999999999994%" id="mcps1.1.3.1.2"><p id="p5893233917230"><a name="p5893233917230"></a><a name="p5893233917230"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row879015617230"><td class="cellrowborder" valign="top" width="46.54%" headers="mcps1.1.3.1.1 "><p id="p4091407017230"><a name="p4091407017230"></a><a name="p4091407017230"></a>400 Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.459999999999994%" headers="mcps1.1.3.1.2 "><p id="p2570540117230"><a name="p2570540117230"></a><a name="p2570540117230"></a>请求错误。</p>
    </td>
    </tr>
    <tr id="row176271617230"><td class="cellrowborder" valign="top" width="46.54%" headers="mcps1.1.3.1.1 "><p id="p856227917230"><a name="p856227917230"></a><a name="p856227917230"></a>401 Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.459999999999994%" headers="mcps1.1.3.1.2 "><p id="p2245600317230"><a name="p2245600317230"></a><a name="p2245600317230"></a>鉴权失败。</p>
    </td>
    </tr>
    <tr id="row77743917230"><td class="cellrowborder" valign="top" width="46.54%" headers="mcps1.1.3.1.1 "><p id="p6297256617230"><a name="p6297256617230"></a><a name="p6297256617230"></a>403 Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.459999999999994%" headers="mcps1.1.3.1.2 "><p id="p50424217230"><a name="p50424217230"></a><a name="p50424217230"></a>没有操作权限。</p>
    </td>
    </tr>
    <tr id="row56011270191147"><td class="cellrowborder" valign="top" width="46.54%" headers="mcps1.1.3.1.1 "><p id="p40619053191147"><a name="p40619053191147"></a><a name="p40619053191147"></a>404 Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.459999999999994%" headers="mcps1.1.3.1.2 "><p id="p1808959191147"><a name="p1808959191147"></a><a name="p1808959191147"></a>找不到资源。</p>
    </td>
    </tr>
    <tr id="row453818617230"><td class="cellrowborder" valign="top" width="46.54%" headers="mcps1.1.3.1.1 "><p id="p3204876017230"><a name="p3204876017230"></a><a name="p3204876017230"></a>500 Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.459999999999994%" headers="mcps1.1.3.1.2 "><p id="p4581273417230"><a name="p4581273417230"></a><a name="p4581273417230"></a>服务内部错误。</p>
    </td>
    </tr>
    <tr id="row966142617230"><td class="cellrowborder" valign="top" width="46.54%" headers="mcps1.1.3.1.1 "><p id="p4437803217230"><a name="p4437803217230"></a><a name="p4437803217230"></a>503 Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.459999999999994%" headers="mcps1.1.3.1.2 "><p id="p3785084317230"><a name="p3785084317230"></a><a name="p3785084317230"></a>服务不可用。</p>
    </td>
    </tr>
    </tbody>
    </table>


