# wxbot-IAT-HOOK
微信机器人开发sdk,微信群机器人开发,微信机器人开发教程,微信机器人开发接口,微信机器人开发框架,微信机器人开发原理,微信机器人开发软件,企业微信机器人开发,微信机器人开发api,微信机器人开发 java,微信机器人开发教程 php

导入地址表是地址表，但是提到了数据目录。数据目录在IMAGE_OPTIONAL HEADER 中的 DataDirectory中，下面回忆一下它的定义：PE文件结构中的一个表结构。在介绍PE文件结构的时候虽然没有提到导入
在可执行文件中使用其他DLL 可执行文件的代码或数据，称为导入或者输入。当PE文件需要运行时，将被系统加载至内存中，此时Windows加载器会定位所有的导入的函数或数据将定位到的内容填写至可执行文件的某个位置供其使用。这个定位是需要借助于可执行文件的导入表来完成的。导入表中存放了所使用的DLL的模块名称及导入的函数名称或函数序号。
在加壳与脱壳的研究中，导入表是非常关键的部分。加壳要尽可能地隐藏或破坏原始的导入表。脱壳一定要找到或者还原或者重建原始的导入表，如果无法还原或修复脱壳后的导入表的话，那么可执行文件仍然是无法运行的。在免杀中也有与导入表相关的内容，比如移动导入表函数、修改导入表描述信息、隐藏导入表。····这些操作都是杀毒软件将特征码定位到了导入表上才需要这样做。不过可以看出。导入表也同样受到杀毒软件的“关注”。既然导入表这么重要，下面先来介绍关于导入表的知识。
  7. 3. 2在数据目录中定位第二个目录，中保存了导入函数的RVA地址，通过该RVA地址可以定位到导入表的具体位置。IMAGE_IMPORT_DESCRIPTOR,被导入的每个DLL描述导入都对应一个IMAGE IMP表的结构体是ORT_DESCRIPTOR结构。也就是说，导入的DLL文件与IMAGEIMPORTDESCRIPTOR是一对一的关系。IMAGE_IMPORT_DESCRIPTOR在文件中是一个数组，但是导入信息中并没有明确地指出导入表的个数，而是以一个导入表中全“0”的IMAGEIMPORT_DESCRIPTOR为结束的。导入表对应的结构体定义如下：typedef struct IMAGE_IMPORT_DESCRIPTORunionDWORDCharacteristics;DWORDoriginalFirstThunk;导入表的数据结构定文即 IMAGE_DIRECTORY_ENTRYIMPORT.该结构体
被D
：1
DWORDDWORDDWORDDWORDIMAGE_IMPORT_DESCRIPTOR;导入表中只有这5个成员，而其中重要的只有3个。分别介绍该结构体中每个成员的含义，具体如下。OriginalFirstThunk:该字段指向导入名称表（导入名称表INT)的RVA,该RVA指向的是一个IMAGE_THUNK_DATA的结构体。TimeDataStamp:该字段可以被忽略，一般为0即可。ForwarderChain:该字段一般为0.Name:该字段为指向DLL名称的RVA地址。FirstThunk:该字段包含导入地址表（导入地址表IAT)的RVA,IAT是一个IMAGETHUNK_DATA的结构体数组。TimeDateStamp:ForwarderChain;Name:FirstThunk;
![image](https://user-images.githubusercontent.com/73727649/196103896-e09fe8ae-c046-4db8-9aa1-227af9f00368.png)
个人微信
目前已经实现了很多有趣的功能，运行稳定，比如：发各种消息，
接收各种消息，群管，下载文件，加好友，检测僵尸粉，朋友圈等等功能，
可提供接口，方便各种语言二次开发，欢迎技术交流，Q：2645542961
，请勿用于商业用途。
![image](https://user-images.githubusercontent.com/73727649/196104038-9be9d9ee-7195-4667-879d-8174c1b581ed.png)

企业微信：
目前已经实现了大部分功能，运行稳定，比如：发各种消息，
接收各种消息，外部群内部群管理，下载文件，加好友等等功能，
可提供接口，方便各种语言二次开发，欢迎技术交流。
