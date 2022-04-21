
 https://dashboard.heroku.com/new?template=https://github.com/plok00286750/123
 
对部署时需设定的变量名称做如下说明。
| 变量 | 默认值 | 说明 |
| :--- | :--- | :--- |
| `USER` | `admin` | 用户名，适用于所有需要输入用户名的页面 |
| `PASSWORD` | `password` | 务必修改为强密码，同样适用于所有需要输入密码的页面 |
| `LANGUAGE` | `en` | 设置导航页和Filebrowser界面语言，chs为中文 |
| `PORTAL_PATH` | `/portal` | 导航页路径和所有Web服务的基础URL，相当于密码之外多一层保护。不能为“/"和空值，结尾不能加“/" |
| `DRIVE_NAME` | `auto` | Rclone远程存储配置名称，默认值auto将从配置文件第一行中提取 |
| `RCLONE_CONFIG_BASE64` | `` | Rclone配置文件Base64编码，可使用linux系统base64命令或者在线base64工具生成 |
| `VMESS_UUID` | `a3ac20a7-45fe-4656-97ee-937ffec46144` | Vmess协议UUID，务必修改，建议使用UUID工具生成 |
| `VMESS_PATH` | `/f495ba1f` | Vmess协议路径，不要包含敏感信息 |
| `TZ` | `UTC` | 时区，Asia/Shanghai为中国时区 |

对控制Aria2和Rclone联动模式的POST_MODE变量说明：
 1. dummy模式为无操作，move模式为下载及做种完成后移动到本地finished目录。
 2. move_remote模式为下载及做种完成后先移动到本地data数据卷下finished目录，然后移动到rclone远程存储。
 3. move_remote_only模式为下载及做种完成后移动到rclone远程存储。
 4. copy_remote_first模式为下载完成后立即复制到rclone远程存储，BT任务在做种前即触发。
 5. copy_remote模式为下载及做种完成后先移动到本地finished目录，然后复制到rclone远程存储。
 6. custom模式为自行设置aria2配置文件触发脚本选项。



 
