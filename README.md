# OCChaos
===========================

----
使用一种廉价的方式来实现在iOS马甲包制作过程中，修改文件md5值，前后缀修改，垃圾代码生成，垃圾代码加入工具。
----

![](./run.gif)

环境依赖

不支持python2

安装步骤

*python要在3以上版本

```
pip install occhaos
```

使用步骤

1.config文件是必须的，必须是json格式，参照格式如下
```
{
  "pre_str":"TY",
  "pre_to_str":"TYZ",
  "suf_set" :[".h", ".m", ".xib", ".storyboard", ".mm"],
  "project_path" : "/Volumes/Files/Document/TestIpa/TestIpa",
  "pbxpro_path": "/Volumes/Files/Document/TestIpa/TestIpa.xcodeproj/project.pbxproj",
  "img_suf_set":[".png", ".jpg"],
  "file_floadPath":"/Volumes/Files/Document/TestIpa/TestIpa",
  "classArray":["NSString", "UILabel", "NSDictionary", "NSData", "UIScrollView", "UIView", "UITextView", "UITableView",
              "UIImageView"],
  "h_file_mark_arr":["l;", "m;", "n;", "q;", "y;"],
  "m_file_mark_arr":["n];", "w];", "m];", "c];", "p];", "q];", "l];"],
  "output_path":"/Volumes/Files/Document/LionMobi/TestIpa/out_put",
  "关于参数的说明（该字段不做修改，其余字段按需修改）":{
    "pre_str":"需要修改的类名前缀 （需替换）",
    "pre_to_str":"新的类名前缀 （需替换）",
    "suf_set" :"需要搜寻以下文件类型 （根据自己需求替换）如 '.h', '.m', '.xib', '.storyboard', '.mm'",
    "project_path" : "项目路径   （找到自己的项目路径）",
    "pbxpro_path": "项目project.pbxproj文件路径 需要更新配置文件中的类名 （找到自己的项目project.pbxproj路径）",
    "img_suf_set":"图片的结尾后缀 数组",
    "file_floadPath":"在目标.h  .m 文件所在的路径",
    "classArray":".h文件里属性的类型从这个数组里随机选(按需修改)",
    "h_file_mark_arr":".h   .m  文件中 需要在哪种标识后面添加废弃代码(按需修改)",
    "m_file_mark_arr":".h   .m  文件中 需要在哪种标识后面添加废弃代码(按需修改)",
    "output_path":"垃圾OC类文件输出目录"
  }
}
```
2.运行
```
occhaos
```
