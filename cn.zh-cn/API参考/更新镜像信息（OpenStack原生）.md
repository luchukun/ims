# 更新镜像信息（OpenStack原生）<a name="ZH-CN_TOPIC_0060804960"></a>

## 功能介绍<a name="section16095919"></a>

修改镜像信息。

## URI<a name="section10645546"></a>

-   URI格式

    PATCH /v2/images/\{image\_id\}

-   参数说明

    URI参数说明

    <a name="table30282311"></a>
    <table><thead align="left"><tr id="row19672999"><th class="cellrowborder" valign="top" width="30.826917308269174%" id="mcps1.1.5.1.1"><p id="p50009058"><a name="p50009058"></a><a name="p50009058"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.858214178582145%" id="mcps1.1.5.1.2"><p id="p24201902"><a name="p24201902"></a><a name="p24201902"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.48795120487951%" id="mcps1.1.5.1.3"><p id="p265296612135"><a name="p265296612135"></a><a name="p265296612135"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="30.826917308269174%" id="mcps1.1.5.1.4"><p id="p14197042"><a name="p14197042"></a><a name="p14197042"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row41227749"><td class="cellrowborder" valign="top" width="30.826917308269174%" headers="mcps1.1.5.1.1 "><p id="p51113363"><a name="p51113363"></a><a name="p51113363"></a>image_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.858214178582145%" headers="mcps1.1.5.1.2 "><p id="p46541742"><a name="p46541742"></a><a name="p46541742"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.48795120487951%" headers="mcps1.1.5.1.3 "><p id="p14189122135"><a name="p14189122135"></a><a name="p14189122135"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.826917308269174%" headers="mcps1.1.5.1.4 "><p id="p11784733"><a name="p11784733"></a><a name="p11784733"></a>镜像ID</p>
    </td>
    </tr>
    </tbody>
    </table>


## 接口约束<a name="section4659381317371"></a>

更新镜像目前只能更新用户自定义属性，或者镜像的名称和描述信息，其他属性不允许用户更新。

## 请求消息<a name="section28701056"></a>

-   Request Body参数说明

    Glance有两种方式的更新操作，通过http header里的Content-Type指定，当前支持“application/openstack-images-v2.0-json-patch”、“application/openstack-images-v2.1-json-patch”两种Content-Type。不同的Content-Type区别只是请求消息体格式不同。

    **表 1**  v2.0版本请求消息体

    <a name="table16631401173819"></a>
    <table><thead align="left"><tr id="row52304254173819"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p8786159173819"><a name="p8786159173819"></a><a name="p8786159173819"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p40590310173819"><a name="p40590310173819"></a><a name="p40590310173819"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p66589640173819"><a name="p66589640173819"></a><a name="p66589640173819"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p25051775173819"><a name="p25051775173819"></a><a name="p25051775173819"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15927923173819"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p15093387173819"><a name="p15093387173819"></a><a name="p15093387173819"></a>replace</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p14604848173819"><a name="p14604848173819"></a><a name="p14604848173819"></a>String</p>
    </td>
    <td class="cellrowborder" rowspan="3" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p42142025173819"><a name="p42142025173819"></a><a name="p42142025173819"></a>取值三选一</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p58060863173819"><a name="p58060863173819"></a><a name="p58060863173819"></a>key为replace表示替换镜像的相关属性，值为所要替换的属性需要在属性名称前加”/”</p>
    </td>
    </tr>
    <tr id="row52785720173819"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p47784899173819"><a name="p47784899173819"></a><a name="p47784899173819"></a>add</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p45371615173819"><a name="p45371615173819"></a><a name="p45371615173819"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p51222195173819"><a name="p51222195173819"></a><a name="p51222195173819"></a>key为add表示添加镜像属性，值为所要添加的属性名称，需要在属性名称前加”/”</p>
    </td>
    </tr>
    <tr id="row58346578173819"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p28452398173819"><a name="p28452398173819"></a><a name="p28452398173819"></a>remove</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p22942935173819"><a name="p22942935173819"></a><a name="p22942935173819"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p46438452173819"><a name="p46438452173819"></a><a name="p46438452173819"></a>key为remove表示删除镜像属性，值为所要删除的属性名称需要在属性名称前加”/”</p>
    </td>
    </tr>
    <tr id="row15292890173819"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p30764577173819"><a name="p30764577173819"></a><a name="p30764577173819"></a>value</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p8902800173819"><a name="p8902800173819"></a><a name="p8902800173819"></a>Mixed</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p50038224173819"><a name="p50038224173819"></a><a name="p50038224173819"></a>根据前面的key决定，replace和add需要指定，remove不需要</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p26564361173819"><a name="p26564361173819"></a><a name="p26564361173819"></a>所需更新/添加的属性的值。参数说明请参考<a href="镜像属性.md#section61598810155254">镜像属性</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  v2.1版本请求消息体

    <a name="table64660774173946"></a>
    <table><thead align="left"><tr id="row19981747173946"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p7908847173946"><a name="p7908847173946"></a><a name="p7908847173946"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p36636838173946"><a name="p36636838173946"></a><a name="p36636838173946"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p14793922173946"><a name="p14793922173946"></a><a name="p14793922173946"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p57457067173946"><a name="p57457067173946"></a><a name="p57457067173946"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row23510856173946"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p25331202173946"><a name="p25331202173946"></a><a name="p25331202173946"></a>op</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p38561472173946"><a name="p38561472173946"></a><a name="p38561472173946"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p36471531173946"><a name="p36471531173946"></a><a name="p36471531173946"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1404010173946"><a name="p1404010173946"></a><a name="p1404010173946"></a>所需进行的更新操作的类型：替换、添加、删除。取值范围：replace、add、remove</p>
    </td>
    </tr>
    <tr id="row12636093173946"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p16890582173946"><a name="p16890582173946"></a><a name="p16890582173946"></a>path</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p25959863173946"><a name="p25959863173946"></a><a name="p25959863173946"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p22374153173946"><a name="p22374153173946"></a><a name="p22374153173946"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p367091173946"><a name="p367091173946"></a><a name="p367091173946"></a>所要操作的属性名称。replace和remove操作取值只能是镜像当前已有的属性、add操作取值只能是镜像当前不存在的属性，需要在属性名称前加”/”</p>
    </td>
    </tr>
    <tr id="row3303825173946"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p66283283173946"><a name="p66283283173946"></a><a name="p66283283173946"></a>value</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p236866173946"><a name="p236866173946"></a><a name="p236866173946"></a>Mixed</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p19186181173946"><a name="p19186181173946"></a><a name="p19186181173946"></a>根据op的value决定，replace、add需要指定，remove不需要</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p10576837173946"><a name="p10576837173946"></a><a name="p10576837173946"></a>所需更新/添加属性的值。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例

    ```
    PATCH /v2/images/33ad552d-1149-471c-8190-ff6776174a00
    ```

    -   V2.0版本请求体

        ```
        "Content-Type:application/openstack-images-v2.0-json-patch"   [       {           "replace": "/name",
                     "value": "test01"       } 
          ]     
        ```

    -   V2.1版本请求体

        ```
        "Content-Type:application/openstack-images-v2.1-json-patch"   [       {           "op":"replace",
                   "path":"/name",
                  "value": "test01"       } 
          ]
        ```



## 响应<a name="section56982912"></a>

-   参数说明

    <a name="table2226228174345"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0020091567_row23919935194835"><th class="cellrowborder" valign="top" width="28.57%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0020091567_p58466603194835"><a name="zh-cn_topic_0020091567_p58466603194835"></a><a name="zh-cn_topic_0020091567_p58466603194835"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.29%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0020091567_p38174436194835"><a name="zh-cn_topic_0020091567_p38174436194835"></a><a name="zh-cn_topic_0020091567_p38174436194835"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="57.14%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0020091567_p5121617194835"><a name="zh-cn_topic_0020091567_p5121617194835"></a><a name="zh-cn_topic_0020091567_p5121617194835"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0020091567_row12197851194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p48501865194835"><a name="zh-cn_topic_0020091567_p48501865194835"></a><a name="zh-cn_topic_0020091567_p48501865194835"></a>file</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p36336996194835"><a name="zh-cn_topic_0020091567_p36336996194835"></a><a name="zh-cn_topic_0020091567_p36336996194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p57615539194835"><a name="zh-cn_topic_0020091567_p57615539194835"></a><a name="zh-cn_topic_0020091567_p57615539194835"></a>镜像文件下载和上传链接。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row48777806194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p58688183194835"><a name="zh-cn_topic_0020091567_p58688183194835"></a><a name="zh-cn_topic_0020091567_p58688183194835"></a>owner</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p56122344194835"><a name="zh-cn_topic_0020091567_p56122344194835"></a><a name="zh-cn_topic_0020091567_p56122344194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p49616010194835"><a name="zh-cn_topic_0020091567_p49616010194835"></a><a name="zh-cn_topic_0020091567_p49616010194835"></a>镜像属于哪个租户。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row43890908194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p65502698194835"><a name="zh-cn_topic_0020091567_p65502698194835"></a><a name="zh-cn_topic_0020091567_p65502698194835"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p4118332194835"><a name="zh-cn_topic_0020091567_p4118332194835"></a><a name="zh-cn_topic_0020091567_p4118332194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p65149499194835"><a name="zh-cn_topic_0020091567_p65149499194835"></a><a name="zh-cn_topic_0020091567_p65149499194835"></a>镜像ID。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row49474582194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p48018243194835"><a name="zh-cn_topic_0020091567_p48018243194835"></a><a name="zh-cn_topic_0020091567_p48018243194835"></a>size</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p64272464194835"><a name="zh-cn_topic_0020091567_p64272464194835"></a><a name="zh-cn_topic_0020091567_p64272464194835"></a>Long</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p38687077194835"><a name="zh-cn_topic_0020091567_p38687077194835"></a><a name="zh-cn_topic_0020091567_p38687077194835"></a>目前暂时不使用。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row12639379194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p17156744194835"><a name="zh-cn_topic_0020091567_p17156744194835"></a><a name="zh-cn_topic_0020091567_p17156744194835"></a>self</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p47519001194835"><a name="zh-cn_topic_0020091567_p47519001194835"></a><a name="zh-cn_topic_0020091567_p47519001194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p23833904194835"><a name="zh-cn_topic_0020091567_p23833904194835"></a><a name="zh-cn_topic_0020091567_p23833904194835"></a>镜像链接信息。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row13178544194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p60829128194835"><a name="zh-cn_topic_0020091567_p60829128194835"></a><a name="zh-cn_topic_0020091567_p60829128194835"></a>schema</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p28212312194835"><a name="zh-cn_topic_0020091567_p28212312194835"></a><a name="zh-cn_topic_0020091567_p28212312194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p3495945194835"><a name="zh-cn_topic_0020091567_p3495945194835"></a><a name="zh-cn_topic_0020091567_p3495945194835"></a>镜像视图。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row31463509194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p65516314194835"><a name="zh-cn_topic_0020091567_p65516314194835"></a><a name="zh-cn_topic_0020091567_p65516314194835"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p5221203194835"><a name="zh-cn_topic_0020091567_p5221203194835"></a><a name="zh-cn_topic_0020091567_p5221203194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p29539523155411"><a name="zh-cn_topic_0020091567_p29539523155411"></a><a name="zh-cn_topic_0020091567_p29539523155411"></a>镜像状态。取值如下：</p>
    <a name="zh-cn_topic_0020091567_ul64671162155411"></a><a name="zh-cn_topic_0020091567_ul64671162155411"></a><ul id="zh-cn_topic_0020091567_ul64671162155411"><li>queued：表示镜像元数据已经创建成功，等待上传镜像文件。</li><li>saving：表示镜像正在上传文件到后端存储。</li><li>deleted：表示镜像已经删除。</li><li>killed：表示镜像上传错误。</li><li>active：表示镜像可以正常使用。</li></ul>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row48160946194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p8722525194835"><a name="zh-cn_topic_0020091567_p8722525194835"></a><a name="zh-cn_topic_0020091567_p8722525194835"></a>tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p35435929194835"><a name="zh-cn_topic_0020091567_p35435929194835"></a><a name="zh-cn_topic_0020091567_p35435929194835"></a>List&lt;String&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p51737997194835"><a name="zh-cn_topic_0020091567_p51737997194835"></a><a name="zh-cn_topic_0020091567_p51737997194835"></a>镜像标签列表，提供用户可以自定义管理私有镜像的能力。用户可以通过镜像标签接口为每个镜像增加不同的标签，在查询接口中可以根据标签进行过滤。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row62988796194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p1818872194835"><a name="zh-cn_topic_0020091567_p1818872194835"></a><a name="zh-cn_topic_0020091567_p1818872194835"></a>visibility</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p13110977194835"><a name="zh-cn_topic_0020091567_p13110977194835"></a><a name="zh-cn_topic_0020091567_p13110977194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p55356222194835"><a name="zh-cn_topic_0020091567_p55356222194835"></a><a name="zh-cn_topic_0020091567_p55356222194835"></a>是否被其他租户可见，取值为private或public。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row28443956194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p22259099194835"><a name="zh-cn_topic_0020091567_p22259099194835"></a><a name="zh-cn_topic_0020091567_p22259099194835"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p58156586194835"><a name="zh-cn_topic_0020091567_p58156586194835"></a><a name="zh-cn_topic_0020091567_p58156586194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p13063050194835"><a name="zh-cn_topic_0020091567_p13063050194835"></a><a name="zh-cn_topic_0020091567_p13063050194835"></a>镜像名称。name参数说明请参考<a href="镜像属性.md#section61598810155254">镜像属性</a>。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row50458592194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p60614140194835"><a name="zh-cn_topic_0020091567_p60614140194835"></a><a name="zh-cn_topic_0020091567_p60614140194835"></a>checksum</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p10798268194835"><a name="zh-cn_topic_0020091567_p10798268194835"></a><a name="zh-cn_topic_0020091567_p10798268194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p2244488194835"><a name="zh-cn_topic_0020091567_p2244488194835"></a><a name="zh-cn_topic_0020091567_p2244488194835"></a>目前暂时不使用。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row20200399194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p25619609194835"><a name="zh-cn_topic_0020091567_p25619609194835"></a><a name="zh-cn_topic_0020091567_p25619609194835"></a>deleted</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p61922468194835"><a name="zh-cn_topic_0020091567_p61922468194835"></a><a name="zh-cn_topic_0020091567_p61922468194835"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p49664024194835"><a name="zh-cn_topic_0020091567_p49664024194835"></a><a name="zh-cn_topic_0020091567_p49664024194835"></a>是否是删除的镜像，取值为true或者false。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row44323032194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p33395835194835"><a name="zh-cn_topic_0020091567_p33395835194835"></a><a name="zh-cn_topic_0020091567_p33395835194835"></a>protected</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p20708123194835"><a name="zh-cn_topic_0020091567_p20708123194835"></a><a name="zh-cn_topic_0020091567_p20708123194835"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p66745247194835"><a name="zh-cn_topic_0020091567_p66745247194835"></a><a name="zh-cn_topic_0020091567_p66745247194835"></a>是否是受保护的，受保护的镜像不允许删除。取值为true或false。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row63836314194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p3358960194835"><a name="zh-cn_topic_0020091567_p3358960194835"></a><a name="zh-cn_topic_0020091567_p3358960194835"></a>container_format</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p3640350194835"><a name="zh-cn_topic_0020091567_p3640350194835"></a><a name="zh-cn_topic_0020091567_p3640350194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p26432973194835"><a name="zh-cn_topic_0020091567_p26432973194835"></a><a name="zh-cn_topic_0020091567_p26432973194835"></a>容器类型。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row36570173194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p9393999194835"><a name="zh-cn_topic_0020091567_p9393999194835"></a><a name="zh-cn_topic_0020091567_p9393999194835"></a>min_ram</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p22716470194835"><a name="zh-cn_topic_0020091567_p22716470194835"></a><a name="zh-cn_topic_0020091567_p22716470194835"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p28094810194835"><a name="zh-cn_topic_0020091567_p28094810194835"></a><a name="zh-cn_topic_0020091567_p28094810194835"></a>镜像运行需要的最小内存，单位为MB。参数取值依据弹性云服务器的规格限制，默认设置为0。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row51176839416"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p118791549416"><a name="zh-cn_topic_0020091567_p118791549416"></a><a name="zh-cn_topic_0020091567_p118791549416"></a>max_ram</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p257405589416"><a name="zh-cn_topic_0020091567_p257405589416"></a><a name="zh-cn_topic_0020091567_p257405589416"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p46104269416"><a name="zh-cn_topic_0020091567_p46104269416"></a><a name="zh-cn_topic_0020091567_p46104269416"></a>镜像支持的最大内存，单位为MB。参数取值可以参考弹性云服务规格限制，默认不设置。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row51526702194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p12913335194835"><a name="zh-cn_topic_0020091567_p12913335194835"></a><a name="zh-cn_topic_0020091567_p12913335194835"></a>updated_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p39347249194835"><a name="zh-cn_topic_0020091567_p39347249194835"></a><a name="zh-cn_topic_0020091567_p39347249194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p33010628194835"><a name="zh-cn_topic_0020091567_p33010628194835"></a><a name="zh-cn_topic_0020091567_p33010628194835"></a>更新时间。格式为UTC时间。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row28660198194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p39774672194835"><a name="zh-cn_topic_0020091567_p39774672194835"></a><a name="zh-cn_topic_0020091567_p39774672194835"></a>__os_bit</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p522982194835"><a name="zh-cn_topic_0020091567_p522982194835"></a><a name="zh-cn_topic_0020091567_p522982194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p42361618194835"><a name="zh-cn_topic_0020091567_p42361618194835"></a><a name="zh-cn_topic_0020091567_p42361618194835"></a>操作系统位数，一般取值为“32”或者“64”。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row45710242194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p11542151194835"><a name="zh-cn_topic_0020091567_p11542151194835"></a><a name="zh-cn_topic_0020091567_p11542151194835"></a>__os_version</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p62499061194835"><a name="zh-cn_topic_0020091567_p62499061194835"></a><a name="zh-cn_topic_0020091567_p62499061194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p29259155194835"><a name="zh-cn_topic_0020091567_p29259155194835"></a><a name="zh-cn_topic_0020091567_p29259155194835"></a>操作系统具体版本。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row62005803194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p56414165194835"><a name="zh-cn_topic_0020091567_p56414165194835"></a><a name="zh-cn_topic_0020091567_p56414165194835"></a>__description</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p6144643194835"><a name="zh-cn_topic_0020091567_p6144643194835"></a><a name="zh-cn_topic_0020091567_p6144643194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p27954078194835"><a name="zh-cn_topic_0020091567_p27954078194835"></a><a name="zh-cn_topic_0020091567_p27954078194835"></a>镜像描述信息。_description参数说明请参考<a href="镜像属性.md#section61598810155254">镜像属性</a>。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row50260111194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p44537208194835"><a name="zh-cn_topic_0020091567_p44537208194835"></a><a name="zh-cn_topic_0020091567_p44537208194835"></a>disk_format</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p50744065194835"><a name="zh-cn_topic_0020091567_p50744065194835"></a><a name="zh-cn_topic_0020091567_p50744065194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p16628562194835"><a name="zh-cn_topic_0020091567_p16628562194835"></a><a name="zh-cn_topic_0020091567_p16628562194835"></a>镜像的格式，目前支持vhd，zvhd、raw，qcow2。默认值是vhd。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row15439333194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p42626486194835"><a name="zh-cn_topic_0020091567_p42626486194835"></a><a name="zh-cn_topic_0020091567_p42626486194835"></a>__isregistered</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p30193380194835"><a name="zh-cn_topic_0020091567_p30193380194835"></a><a name="zh-cn_topic_0020091567_p30193380194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p29744726194835"><a name="zh-cn_topic_0020091567_p29744726194835"></a><a name="zh-cn_topic_0020091567_p29744726194835"></a>是否是注册过的镜像，取值为“true”或者“false”。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row66375949194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p7742752194835"><a name="zh-cn_topic_0020091567_p7742752194835"></a><a name="zh-cn_topic_0020091567_p7742752194835"></a>__platform</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p23183213194835"><a name="zh-cn_topic_0020091567_p23183213194835"></a><a name="zh-cn_topic_0020091567_p23183213194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p16267923202620"><a name="zh-cn_topic_0020091567_p16267923202620"></a><a name="zh-cn_topic_0020091567_p16267923202620"></a>镜像平台分类，取值为Windows，Ubuntu，RedHat，SUSE，CentOS，Debian，OpenSUSE, Oracle Linux，Fedora，Other，CoreOS和EulerOS。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row56237676194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p58957901194835"><a name="zh-cn_topic_0020091567_p58957901194835"></a><a name="zh-cn_topic_0020091567_p58957901194835"></a>__os_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p10860642194835"><a name="zh-cn_topic_0020091567_p10860642194835"></a><a name="zh-cn_topic_0020091567_p10860642194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p7296787194835"><a name="zh-cn_topic_0020091567_p7296787194835"></a><a name="zh-cn_topic_0020091567_p7296787194835"></a>操作系统类型，目前取值Linux， Windows，Other。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row65671090194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p17758106194835"><a name="zh-cn_topic_0020091567_p17758106194835"></a><a name="zh-cn_topic_0020091567_p17758106194835"></a>min_disk</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p29120466194835"><a name="zh-cn_topic_0020091567_p29120466194835"></a><a name="zh-cn_topic_0020091567_p29120466194835"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p9947522194835"><a name="zh-cn_topic_0020091567_p9947522194835"></a><a name="zh-cn_topic_0020091567_p9947522194835"></a>镜像运行需要的最小磁盘容量，单位为GB 。取值为40～1024GB。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row22418839194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p3986671194835"><a name="zh-cn_topic_0020091567_p3986671194835"></a><a name="zh-cn_topic_0020091567_p3986671194835"></a>virtual_env_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p54484948194835"><a name="zh-cn_topic_0020091567_p54484948194835"></a><a name="zh-cn_topic_0020091567_p54484948194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p51204653194835"><a name="zh-cn_topic_0020091567_p51204653194835"></a><a name="zh-cn_topic_0020091567_p51204653194835"></a>镜像使用环境类型：FusionCompute，Ironic，DataImage。如果弹性云服务器镜像，则取值为FusionCompute，如果是数据卷镜像则取值是DataImage，如果是裸金属服务器镜像，则取值是Ironic。。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row58188697194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p15663996194835"><a name="zh-cn_topic_0020091567_p15663996194835"></a><a name="zh-cn_topic_0020091567_p15663996194835"></a>__image_source_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p60824135194835"><a name="zh-cn_topic_0020091567_p60824135194835"></a><a name="zh-cn_topic_0020091567_p60824135194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p27807907194835"><a name="zh-cn_topic_0020091567_p27807907194835"></a><a name="zh-cn_topic_0020091567_p27807907194835"></a>镜像后端存储类型，目前只支持uds。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row48944575194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p5087606194835"><a name="zh-cn_topic_0020091567_p5087606194835"></a><a name="zh-cn_topic_0020091567_p5087606194835"></a>__imagetype</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p9442962194835"><a name="zh-cn_topic_0020091567_p9442962194835"></a><a name="zh-cn_topic_0020091567_p9442962194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p2572734285718"><a name="zh-cn_topic_0020091567_p2572734285718"></a><a name="zh-cn_topic_0020091567_p2572734285718"></a>镜像类型，目前支持：</p>
    <a name="zh-cn_topic_0020091567_ul6291210685828"></a><a name="zh-cn_topic_0020091567_ul6291210685828"></a><ul id="zh-cn_topic_0020091567_ul6291210685828"><li>公共镜像（gold）</li><li>私有镜像（private）</li><li>共享镜像（shared）</li></ul>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row38815832194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p57074654194835"><a name="zh-cn_topic_0020091567_p57074654194835"></a><a name="zh-cn_topic_0020091567_p57074654194835"></a>created_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p59644261194835"><a name="zh-cn_topic_0020091567_p59644261194835"></a><a name="zh-cn_topic_0020091567_p59644261194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p66455828194835"><a name="zh-cn_topic_0020091567_p66455828194835"></a><a name="zh-cn_topic_0020091567_p66455828194835"></a>创建时间。格式为UTC时间。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row61231547194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p60808250194835"><a name="zh-cn_topic_0020091567_p60808250194835"></a><a name="zh-cn_topic_0020091567_p60808250194835"></a>virtual_size</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p26521206194835"><a name="zh-cn_topic_0020091567_p26521206194835"></a><a name="zh-cn_topic_0020091567_p26521206194835"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p734038194835"><a name="zh-cn_topic_0020091567_p734038194835"></a><a name="zh-cn_topic_0020091567_p734038194835"></a>目前暂时不使用。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row6606343194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p65351769194835"><a name="zh-cn_topic_0020091567_p65351769194835"></a><a name="zh-cn_topic_0020091567_p65351769194835"></a>deleted_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p59001923194835"><a name="zh-cn_topic_0020091567_p59001923194835"></a><a name="zh-cn_topic_0020091567_p59001923194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p14426478194835"><a name="zh-cn_topic_0020091567_p14426478194835"></a><a name="zh-cn_topic_0020091567_p14426478194835"></a>删除时间。格式为UTC时间。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row62729443194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p47920146194835"><a name="zh-cn_topic_0020091567_p47920146194835"></a><a name="zh-cn_topic_0020091567_p47920146194835"></a>__originalimagename</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p56326613194835"><a name="zh-cn_topic_0020091567_p56326613194835"></a><a name="zh-cn_topic_0020091567_p56326613194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p66161813194835"><a name="zh-cn_topic_0020091567_p66161813194835"></a><a name="zh-cn_topic_0020091567_p66161813194835"></a>父镜像ID。</p>
    <p id="zh-cn_topic_0020091567_p58585407194835"><a name="zh-cn_topic_0020091567_p58585407194835"></a><a name="zh-cn_topic_0020091567_p58585407194835"></a>公共镜像或通过文件创建的私有镜像，取值为空。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row57506617194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p27524394194835"><a name="zh-cn_topic_0020091567_p27524394194835"></a><a name="zh-cn_topic_0020091567_p27524394194835"></a>__backup_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p14883407194835"><a name="zh-cn_topic_0020091567_p14883407194835"></a><a name="zh-cn_topic_0020091567_p14883407194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p64705296194835"><a name="zh-cn_topic_0020091567_p64705296194835"></a><a name="zh-cn_topic_0020091567_p64705296194835"></a>备份ID。如果是备份创建的镜像，则填写为备份的ID，否则为空。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row45476759194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p59738895194835"><a name="zh-cn_topic_0020091567_p59738895194835"></a><a name="zh-cn_topic_0020091567_p59738895194835"></a>__productcode</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p7012311194835"><a name="zh-cn_topic_0020091567_p7012311194835"></a><a name="zh-cn_topic_0020091567_p7012311194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p31126295194835"><a name="zh-cn_topic_0020091567_p31126295194835"></a><a name="zh-cn_topic_0020091567_p31126295194835"></a>市场镜像的产品ID。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row54629742194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p62932961194835"><a name="zh-cn_topic_0020091567_p62932961194835"></a><a name="zh-cn_topic_0020091567_p62932961194835"></a>__image_size</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p64405052194835"><a name="zh-cn_topic_0020091567_p64405052194835"></a><a name="zh-cn_topic_0020091567_p64405052194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p49426728194835"><a name="zh-cn_topic_0020091567_p49426728194835"></a><a name="zh-cn_topic_0020091567_p49426728194835"></a>镜像文件的大小，单位为字节。必须大于0。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row42187372194835"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p61733939194835"><a name="zh-cn_topic_0020091567_p61733939194835"></a><a name="zh-cn_topic_0020091567_p61733939194835"></a>__data_origin</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p34393183194835"><a name="zh-cn_topic_0020091567_p34393183194835"></a><a name="zh-cn_topic_0020091567_p34393183194835"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p34384472194835"><a name="zh-cn_topic_0020091567_p34384472194835"></a><a name="zh-cn_topic_0020091567_p34384472194835"></a>镜像来源。</p>
    <p id="zh-cn_topic_0020091567_p41024797194835"><a name="zh-cn_topic_0020091567_p41024797194835"></a><a name="zh-cn_topic_0020091567_p41024797194835"></a>公共镜像为空。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row1922712020747"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p1688848719937"><a name="zh-cn_topic_0020091567_p1688848719937"></a><a name="zh-cn_topic_0020091567_p1688848719937"></a>__support_kvm</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p1314210319937"><a name="zh-cn_topic_0020091567_p1314210319937"></a><a name="zh-cn_topic_0020091567_p1314210319937"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p6435151319937"><a name="zh-cn_topic_0020091567_p6435151319937"></a><a name="zh-cn_topic_0020091567_p6435151319937"></a>如果镜像支持KVM，取值为true，否则无需增加该属性。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row2176677820925"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p4682508419937"><a name="zh-cn_topic_0020091567_p4682508419937"></a><a name="zh-cn_topic_0020091567_p4682508419937"></a>__support_xen</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p2922074219937"><a name="zh-cn_topic_0020091567_p2922074219937"></a><a name="zh-cn_topic_0020091567_p2922074219937"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p5999426419937"><a name="zh-cn_topic_0020091567_p5999426419937"></a><a name="zh-cn_topic_0020091567_p5999426419937"></a>如果镜像支持XEN，取值为true，否则无需增加该属性。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row27314678185940"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p5257634319937"><a name="zh-cn_topic_0020091567_p5257634319937"></a><a name="zh-cn_topic_0020091567_p5257634319937"></a>__support_diskintensive</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p4365124719937"><a name="zh-cn_topic_0020091567_p4365124719937"></a><a name="zh-cn_topic_0020091567_p4365124719937"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p3727279719937"><a name="zh-cn_topic_0020091567_p3727279719937"></a><a name="zh-cn_topic_0020091567_p3727279719937"></a>表示该镜像是否支持密集存储性特性。如果镜像支持密集存储性能，则值为true，否则无需增加该属性。镜像操作系统类型请参考<a href="相关参数取值列表.md#table48545918250">表3</a>。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row55915043185940"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p6005168719937"><a name="zh-cn_topic_0020091567_p6005168719937"></a><a name="zh-cn_topic_0020091567_p6005168719937"></a>__support_highperformance</p>
    <p id="zh-cn_topic_0020091567_p3908507319937"><a name="zh-cn_topic_0020091567_p3908507319937"></a><a name="zh-cn_topic_0020091567_p3908507319937"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p6702872519937"><a name="zh-cn_topic_0020091567_p6702872519937"></a><a name="zh-cn_topic_0020091567_p6702872519937"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p3306819319937"><a name="zh-cn_topic_0020091567_p3306819319937"></a><a name="zh-cn_topic_0020091567_p3306819319937"></a>表示该镜像是否支持高计算性能的特性。如果镜像支持高计算性能，则值为true，否则无需增加该属性。镜像操作系统类型请参考<a href="相关参数取值列表.md#table48545918250">表3</a>。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row32822185940"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p1241378919937"><a name="zh-cn_topic_0020091567_p1241378919937"></a><a name="zh-cn_topic_0020091567_p1241378919937"></a>__support_xen_gpu_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p3786179019937"><a name="zh-cn_topic_0020091567_p3786179019937"></a><a name="zh-cn_topic_0020091567_p3786179019937"></a>String</p>
    <p id="zh-cn_topic_0020091567_p5445889719937"><a name="zh-cn_topic_0020091567_p5445889719937"></a><a name="zh-cn_topic_0020091567_p5445889719937"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p5825807419937"><a name="zh-cn_topic_0020091567_p5825807419937"></a><a name="zh-cn_topic_0020091567_p5825807419937"></a>表示该镜像是否支持XEN虚拟化平台下的GPU优化类型的特性，取值参考<a href="相关参数取值列表.md#table65768383152758">表2</a>。镜像操作系统类型请参考<a href="相关参数取值列表.md#table48545918250">表3</a>。如果不支持XEN虚拟化下GPU类型，无需添加该属性。该属性与“__support_xen”和“__support_kvm”属性不共存。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020091567_row14404162162510"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0020091567_p1429443210255"><a name="zh-cn_topic_0020091567_p1429443210255"></a><a name="zh-cn_topic_0020091567_p1429443210255"></a>enterprise_project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.29%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0020091567_p12294143292518"><a name="zh-cn_topic_0020091567_p12294143292518"></a><a name="zh-cn_topic_0020091567_p12294143292518"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.14%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0020091567_p10305182217584"><a name="zh-cn_topic_0020091567_p10305182217584"></a><a name="zh-cn_topic_0020091567_p10305182217584"></a>表示当前镜像所属的企业项目。</p>
    <a name="zh-cn_topic_0020091567_ul76914342313"></a><a name="zh-cn_topic_0020091567_ul76914342313"></a><ul id="zh-cn_topic_0020091567_ul76914342313"><li>取值为0或无该值，表示属于default企业项目。</li><li>取值为UUID，表示属于该UUID对应的企业项目。<p id="zh-cn_topic_0020091567_p14686203192413"><a name="zh-cn_topic_0020091567_p14686203192413"></a><a name="zh-cn_topic_0020091567_p14686203192413"></a>关于企业项目ID的获取及企业项目特性的详细信息，请参考《企业管理用户指南》。</p>
    </li></ul>
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
        "file": "/v2/images/33ad552d-1149-471c-8190-ff6776174a00/file",  
        "owner": "0b1e494e2660441a957313163095fe5c",  
        "id": "33ad552d-1149-471c-8190-ff6776174a00",  
        "size": 2,  
        "self": "/v2/images/33ad552d-1149-471c-8190-ff6776174a00",  
        "schema": "/v2/schemas/image",  
        "status": "active",  
        "tags": [],  
        "visibility": "private",  
        "name": "ims_test",  
        "checksum": "99914b932bd37a50b983c5e7c90ae93b",  
        "deleted": false,  
        "protected": false,  
        "container_format": "bare",  
        "min_ram": 0,  
        "updated_at": "2015-12-08T02:30:49Z",  
        "__os_bit": "64",  
        "__os_version": "Ubuntu 14.04 server 64bit",  
        "__description": "ims test",  
        "disk_format": "vhd",  
        "__isregistered": "true",  
        "__platform": "Ubuntu",  
        "__os_type": "Linux",  
        "min_disk": 40,  
        "virtual_env_type": "FusionCompute",  
        "__image_source_type": "uds",  
        "__imagetype": "private",  
        "created_at": "2015-12-04T09:45:33Z",  
        "virtual_size": 0,  
        "deleted_at": null,  
        "__originalimagename": "33ad552d-1149-471c-8190-ff6776174a00",  
        "__backup_id": "",  
        "__productcode": "",  
        "__image_size": "449261568",  
        "__data_origin": null  
    }
    ```


## 返回值<a name="section43084165"></a>

-   正常

    200

-   异常

    <a name="table2933833017254"></a>
    <table><thead align="left"><tr id="row5083298917254"><th class="cellrowborder" valign="top" width="38.080000000000005%" id="mcps1.1.3.1.1"><p id="p2383143117254"><a name="p2383143117254"></a><a name="p2383143117254"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="61.919999999999995%" id="mcps1.1.3.1.2"><p id="p5129777817254"><a name="p5129777817254"></a><a name="p5129777817254"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row6147936617254"><td class="cellrowborder" valign="top" width="38.080000000000005%" headers="mcps1.1.3.1.1 "><p id="p1377271317254"><a name="p1377271317254"></a><a name="p1377271317254"></a>400 Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.919999999999995%" headers="mcps1.1.3.1.2 "><p id="p4184800617254"><a name="p4184800617254"></a><a name="p4184800617254"></a>请求错误，具体返回错误码请参<a href="错误码.md">错误码</a>。</p>
    </td>
    </tr>
    <tr id="row3424531517254"><td class="cellrowborder" valign="top" width="38.080000000000005%" headers="mcps1.1.3.1.1 "><p id="p2240711217254"><a name="p2240711217254"></a><a name="p2240711217254"></a>401 Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.919999999999995%" headers="mcps1.1.3.1.2 "><p id="p303679817254"><a name="p303679817254"></a><a name="p303679817254"></a>鉴权失败。</p>
    </td>
    </tr>
    <tr id="row2733118717254"><td class="cellrowborder" valign="top" width="38.080000000000005%" headers="mcps1.1.3.1.1 "><p id="p6634251617254"><a name="p6634251617254"></a><a name="p6634251617254"></a>403 Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.919999999999995%" headers="mcps1.1.3.1.2 "><p id="p503474717254"><a name="p503474717254"></a><a name="p503474717254"></a>没有操作权限。</p>
    </td>
    </tr>
    <tr id="row48054866192311"><td class="cellrowborder" valign="top" width="38.080000000000005%" headers="mcps1.1.3.1.1 "><p id="p47142447192313"><a name="p47142447192313"></a><a name="p47142447192313"></a>404 Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.919999999999995%" headers="mcps1.1.3.1.2 "><p id="p60441878192313"><a name="p60441878192313"></a><a name="p60441878192313"></a>找不到资源。</p>
    </td>
    </tr>
    <tr id="row4531272317254"><td class="cellrowborder" valign="top" width="38.080000000000005%" headers="mcps1.1.3.1.1 "><p id="p4645193117254"><a name="p4645193117254"></a><a name="p4645193117254"></a>500 Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.919999999999995%" headers="mcps1.1.3.1.2 "><p id="p451004317254"><a name="p451004317254"></a><a name="p451004317254"></a>服务内部错误。</p>
    </td>
    </tr>
    <tr id="row4059039217254"><td class="cellrowborder" valign="top" width="38.080000000000005%" headers="mcps1.1.3.1.1 "><p id="p6659632017254"><a name="p6659632017254"></a><a name="p6659632017254"></a>503 Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.919999999999995%" headers="mcps1.1.3.1.2 "><p id="p2559285317254"><a name="p2559285317254"></a><a name="p2559285317254"></a>服务不可用。</p>
    </td>
    </tr>
    </tbody>
    </table>


