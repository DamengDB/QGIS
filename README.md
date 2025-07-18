# QGIS
该仓库主要提供了支持达梦数据数据库的QGIS，在QGIS3.41版本分支基础上新增了达梦数据库的支持。

## 主要功能
支持QGIS的Browser(浏览器)功能，具有查看数据库模式、表/视图和字段相关信息的展示和编辑、执行SQL等数据库基本功能。
对于空间数据表，支持图形预览、空间数据的编辑修改、表数据和项目的导入导出、空间数据表的属性和数据源信息查看等功能。

## 使用方法
平台上编译方法同QGIS，可参考https://github.com/qgis/QGIS 。在确保能正确完成QGIS编译基础上，configure阶段编译选项中需要勾选“WITH_DAMENG”选项，generate时编写DAMENG_LIBRARY和DAMENG_INCLUDE_DIR文件路径，指定dmdpi文件(一般在目录\driver\dpi\，包括头文件和dmdpi库文件)位置即可。

在CMake执行完成之后，打开生成的项目文件，即可看到provider_dameng项目。在使用QGIS执行达梦相关SQL语句及空间数据部分功能过程中，可以参考达梦手册帮助使用。




