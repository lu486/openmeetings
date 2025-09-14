## Apache OpenMeetings

![About Openmeetings Logo](/openmeetings-server/src/site/resources/images/logo.png)

[Apache OpenMeetings](https://openmeetings.apache.org) 提供以下功能：
 - [x] **视频会议**（视频会议）
 - [x] **instant messaging**（即时消息）
 - [x] **white board**（白板协作）
 - [x] **collaborative document editing**（协作文档编辑）
 - [x] **other groupware tools**（其他群件工具）

该项目使用用于远程控制和流媒体的媒体服务器API功能 [Kurento](https://www.kurento.org)。

> **中文备注**：Apache OpenMeetings 是一个开源的视频会议和协作平台，提供了完整的在线会议解决方案，支持多人实时视频、音频、聊天和协作编辑等功能。

### 入门指南
获取最新信息，请访问项目网站：
  - [OpenMeetings 官方网站](https://openmeetings.apache.org/)

安装和升级文档可在此处找到：
  - [安装指南](https://openmeetings.apache.org/installation.html)
  - [升级说明](https://openmeetings.apache.org/Upgrade.html)

所有可用的邮件列表在此列出：
  - [邮件列表](https://openmeetings.apache.org/mailing-lists.html)

> **中文备注**：官方网站提供了详细的使用指南和API文档，新用户可以通过安装指南快速搭建环境。

### 系统要求
构建 Apache OpenMeeting 需要以下软件：
- [Apache Maven 3.8.7 或更高版本](https://maven.apache.org/)

运行 Apache OpenMeetings 需要以下软件：
- [Java SE 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)

> **中文备注**：从版本8.0.0开始，项目需要Java 17环境运行，早期版本（如5.0.0及以上）需要Java 11，更早版本则支持Java 8。

### 构建和运行
从源代码构建和运行项目：
1. 确保安装了所需的软件。
2. 在根目录中使用Maven构建项目：
   ```
   mvn clean install -PallModules
   ```
3. 运行OpenMeetings：
   - 导航到 `openmeetings-server/target` 目录。
   - 解压 `apache-openmeetings-x.x.x.tar.gz`（Windows系统使用 `apache-openmeetings-x.x.x.zip`）。
   - 进入 `apache-openmeetings-x.x.x` 目录并执行启动脚本：
     ```
     ./bin/startup.sh
     ```
     （Windows系统使用 `./bin/startup.bat`。）
4. 详细的构建文档：[构建说明](https://openmeetings.apache.org/BuildInstructions.html)

> **中文备注**：`-PallModules` 参数表示构建所有模块，包括前端和后端组件。构建完成后，可以通过启动脚本来启动服务器。

### 构建和持续集成
| 描述                | Jenkins CI                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 主分支每晚构建      | [![构建状态](https://ci-builds.apache.org/job/OpenMeetings/job/openmeetings/badge/icon)](https://ci-builds.apache.org/job/OpenMeetings/job/openmeetings/)       |
| 主分支拉取请求      | [![构建状态](https://ci-builds.apache.org/job/OpenMeetings/job/openmeetings-pr-build/badge/icon)](https://ci-builds.apache.org/job/OpenMeetings/job/openmeetings-pr-build/) |

### 版本说明
详细日志请参阅 [CHANGELOG.md](/CHANGELOG.md) 文件。

### 最新版本


<details>
	<summary>Release 8.1.0 - 安全更新。</summary>

8.1.0
-----
[Release 8.1.0](https://www.apache.org/dyn/closer.lua/openmeetings/8.1.0) 提供以下改进：

安全:
* 所有库都已更新到最新版本

白板:
* 白板视频播放器控件已修复

其他修复和改进，共解决了9个问题
</details>
<details>
	<summary>Release 8.0.0 - 安全更新，迁移到Tomcat 11和Jakarta技术栈。</summary>

8.0.0
-----
[Release 8.0.0](https://www.apache.org/dist/openmeetings/8.0.0) 提供以下改进：

安全:
* OM已迁移到Jakarta技术栈
* 所有库都已更新到最新版本

用户界面:
* 使用Fullcalendar v6

***解决了1个安全漏洞***

其他修复和改进，共解决了8个问题
</details>
<details>
	<summary>Release 7.2.0 - 需要Java 17和KMS 6.18.0+。包含安全、UI和其他改进。</summary>

7.2.0
-----
[Release 7.2.0](https://www.apache.org/dist/openmeetings/7.2.0) 提供以下改进：

重要提示：需要Java 17和KMS 6.18.0+ 

安全:
* 登录/电子邮件现在以不区分大小写的方式处理
* 消息和联系人：消息文件夹不会在用户之间共享
* 所有依赖项都已更新到最新版本

用户界面:
* 过大的个人资料图片现在会被调整大小
* 房间在RTL模式下看起来更好
* 电子邮件消息看起来更好

其他修复和改进，共解决了10个问题
</details>
<details>
	<summary>Release 7.1.0 - 各种安全更新和稳定性修复。</summary>

7.1.0
-----
[Release 7.1.0](https://archive.apache.org/dist/openmeetings/7.1.0) 提供以下改进：

重要提示：需要Java 17和KMS 6.18.0+ 

安全:
* 邀请哈希检查更加严格
* 用户权限集已修复
* 在Admin->Config中输入的路径正在被验证
* 所有依赖项都已更新到最新版本

稳定性:
* TURN服务器配置传递给客户端

***解决了3个安全漏洞***

其他修复和改进，共解决了12个问题
</details>
<details>
	<summary>旧版本详细信息：</summary>

7.0.0
-----
[Release 7.0.0](https://archive.apache.org/dist/openmeetings/7.0.0) 提供以下改进：

重要提示：需要Java 17

用户界面和安全:
* 麦克风开/关不会中断流媒体
* Safari浏览器的稳定性修复
* 白板全屏模式
* 白板重做工具
* 双因素认证
* 库已更新到最新版本

其他修复和改进，共解决了28个问题


6.3.0
-----
[Release 6.3.0](https://archive.apache.org/dist/openmeetings/6.3.0) 提供以下改进：

稳定性和用户界面:
* 多个白板修复
* 确认弹窗已统一
* 最新版Safari浏览器的多个修复
* 库已更新到最新版本

其他修复和改进，共解决了26个问题


6.2.0
-----
[Release 6.2.0](https://archive.apache.org/dist/openmeetings/6.2.0), provides following improvements:

UI improvements, stability fixes, mobile version and adds OpenAPI spec in 3.0.x format

Stability and UI:
* UI fixes
* Modal PopUpFix
* Upgrade to Bootstrap5
* Fixes for Mobile Version and landscape mode
* Improve ability for starting from Home Screen on Mobile device

Integration:
* OpenAPI Spec in swagger format see https://openmeetings.apache.org/swagger
* Improved Integration examples for Node and PHP

Some other fixes and improvements, 28 issues were addressed


6.1.0
-----
[Release 6.1.0](https://archive.apache.org/dist/openmeetings/6.1.0), provides following improvements:

This release provides WebRTC audio/video/screen-sharing in the Room

Stability:
* Room is more stable
* Screen sharing on Safari is fixed
* Recording in interview room is fixed

UI:
* OM theme can selected in Admin -> Config
* Configurable Extra menu is added to the rooms
* Date/time picker is better localized

Some other fixes and improvements, 27 issues were addressed


6.0.0
-----
[Release 6.0.0](https://archive.apache.org/dist/openmeetings/6.0.0), provides following improvements:

This release provides WebRTC audio/video/screen-sharing in the Room

Security:
* TLS1.2. is used for OAuth
* NetTest client count can be limited
* Captcha is now configurable
* Recordings can be globally disabled

Stability:
* Audio/video in room is more stable

UI:
* Translations are improved
* Invitation form displayes time in client time zone
* Notifications are displayed using JS Notification API
* Video pods size can be fixed and configurable per-user

Some other fixes and improvements, 40 issues were addressed


5.1.0
-----
[Release 5.1.0](https://archive.apache.org/dist/openmeetings/5.1.0), provides following improvements:

This release provides WebRTC audio/video/screen-sharing in the Room

Stability:
* Room Audio/Video should be more stable
* OM should work as expected after KMS server restart
* Backup is further improved
* Audio/Video connection established faster
* Most recent versions of dependencies are used

UI:
* User display name is used almost everywhere
* Browser notifications are used to notify about new chat messages and moderator actions
* Interview room was broken
* Mute and "Mic status" were broken

Some other fixes and improvements, 52 issues were addressed


5.0.1
-----
[Release 5.0.1](https://archive.apache.org/dist/openmeetings/5.0.1), provides following improvements:

This release provides WebRTC audio/video/screen-sharing in the Room

Security:
* Rate limit is checked for network test web service
* Libraries are updated to latest versions
* Password complexity can be fine-tuned

Backup/Restore:
* Group files/recordings might be restored to wrong group

UI:
* Translations and support of RTL languages are improved
* Dashboard widgets and personal room are always displayed in current user language

Some other fixes and improvements, 21 issues were addressed


5.0.0
-----
[Release 5.0.0](https://archive.apache.org/dist/openmeetings/5.0.0), provides following improvements:

This release provides WebRTC audio/video/screen-sharing in the Room

IMPORTANT: Java 11 is required

Flash plugin is no longer required in the browser

Security:
* Libraries are updated to latest versions
* More strict CSP is implemented
* User accounts are hidden for regular users
* User email addresses are hidden

UI:
* Support for touch events is added (mobiles, tablets)
* Better support for new MS Edge browser
* Direct link for entering the room with room name (not ID)
* Front camera is used by default
* User avatar is editable at Admin->Users

Audio/Video:
* Stability is improved
* Connection to KMS is auto-recovering
* Camera resolution changes take effect immediately
* Multiple client-side JS errors are fixed

Some other fixes and improvements, 74 issues were addressed


4.0.11
-----
[Release 4.0.11](https://archive.apache.org/dist/openmeetings/4.0.11), provides following improvements:

Security:
* 3rd-party libraries are updated to latest versions
* Email sending via SSL is added
* User email addresses are hidden

Other fixes and improvements, 11 issues were addressed


5.0.0-M4
-----
[Release 5.0.0-M4](https://archive.apache.org/dist/openmeetings/5.0.0-M4), provides following improvements:

This release provides WebRTC audio/video/screen-sharing in the Room

IMPORTANT: Java 11 is required

Flash plugin is no more required in the browser

UI:
* Main UI library has been changed Jquery-UI -> Bootstrap
* Hotkey to resize&arrage "video" windows is added
* Camera/Microphone on/off icons are less confusing
* The room can be blocked until moderator will enter
* Room sidebar dock button works as expected
* Right-click menu for WB tab is fixed
* Link to privacy statement is added to sign-in dialog

Audio/Video:
* Audio-only clients doesn't create "video" windows
* Audio/Video stream tries to re-connect in case of any issue

Backup/Restore:
* Backup/restore was re-worked and better covered with tests
* Multiple other issues are addressed

Integration:
* OAuth: user attributes retrieval is improved
* LDAP documentation is improved
* User picture can be retrieved from LDAP

Please NOTE: this version might be not production ready

Some other fixes and improvements, 56 issues were addressed


5.0.0-M3
-----
[Release 5.0.0-M3](https://archive.apache.org/dist/openmeetings/5.0.0-M3), provides following improvements:

This release provides WebRTC audio/video/screen-sharing in the Room

IMPORTANT: Java 11 is required

Flash plugin is no more required in the browser

Backup/Restore:
* Multiple issues with restore were fixed
* Confirmation of backup import was added
* File/recording hashes are preserved when possible

White board:
* Document upload/conversion is improved
* Whiteboards are not auto-created on room enter
* Keyboard shortcut for quick poll is added

Room:
* User list is now sorted

Audio/Video:
* Multiple issues with audio/video/screen sharing are fixed

Please NOTE: this version might be not production ready

Some other fixes and improvements, 36 issues were addressed


5.0.0-M2
-----
[Release 5.0.0-M2](https://archive.apache.org/dist/openmeetings/5.0.0-M2), provides following improvements:

This release provides WebRTC audio/video/screen-sharing in the Room

IMPORTANT: Java 11 is required

Flash plugin is no more required in the browser

Backup/Restore:
* OAuth configs were not properly backup

White board:
* Math formula is improved
* Room files are improved
* Clean WB REST method perform real-time clean

Room:
* Rooms can be customized on group basis
* "Ghost" users are not displayed in the room
* External user name is displayed as expected

Please NOTE: this version might be not production ready

Some other fixes and improvements, 18 issues were addressed


4.0.9
-----
[Release 4.0.9](https://archive.apache.org/dist/openmeetings/4.0.9), provides following improvements:

Backup/Restore:
* Recordings of deleted users were restored as public
* OAuth configs were not properly backup

White board:
* Math formula is improved
* Room files are improved
* Clean WB REST method perform real-time clean

Room User list:
* "Ghost" users are not displayed in the room
* External user name is displayed as expected

Other fixes and improvements, 19 issues were addressed


5.0.0-M1
-----
[Release 5.0.0-M1](https://archive.apache.org/dist/openmeetings/5.0.0-M1), provides following improvements:

This release provides WebRTC audio/video/screen-sharing in the Room

Flash plugin is no more required in the browser

Please NOTE: this version might be not production ready

Some other fixes and improvements, 30 issues were addressed


4.0.8
-----
[Release 4.0.8](https://archive.apache.org/dist/openmeetings/4.0.8), provides following improvements:

Mobile client:
* Mobile clients are displayed in user list
* Audio/Video switching is more stable

OAuth:
* VK based OAuth login is fixed
* Integrate Wso2 Identity Server

Activities&Actions:
* Less actions for non-moderators
* No duplicated actions are displayed

White board:
* Video on WB works in latest Safari
* White Out tool is added
* Whiteboard size can be tuned
* Link to LaTeX guide is added

Room User list:
* Issue with user's display name is fixed
* "Ghost" users are not displayed in the room

Other fixes and improvements, 30 issues were addressed


4.0.7
-----
[Release 4.0.7](https://archive.apache.org/dist/openmeetings/4.0.7), provides following improvements:

* kick function in RoomWebService is fixed
* Reply button is added to Private Message
* Multiple issues are fixed in Room
* Save white board as JPG is removed
* HttpClient in AppointmentManager is updated 3.x to 4.x
* "endless" invitations can now be invalidated
* Ability to chose user display name is added
* Delete white board object using mouse is now possible
* Ability to duplicate room poll is added
* Health check web service API is added
* OAuth2 authorization can be done via HTTP header
* cliparts can be in SVG format

Other fixes and improvements, 18 issues were addressed


4.0.6
-----
[Release 4.0.6](https://archive.apache.org/dist/openmeetings/4.0.6), provides following improvements:

* Multiple issues with device list retrieval in Settings dialog
* Web services were improved
* Multiple issues with room recording
* Frontend self registering

Other fixes and improvements, 16 issues were addressed


4.0.5
-----
[Release 4.0.5](https://archive.apache.org/dist/openmeetings/4.0.5), provides following improvements:

Room:
* Interview room is improved: re-designed, multiple video windows are supported
* Multiple improvements in Admin
* File tree is improved
* Multiple improvements in white boards

Other fixes and improvements, 24 issues were addressed

4.0.4
-----
[Release 4.0.4](https://archive.apache.org/dist/openmeetings/4.0.4), provides following improvements:

The purpose of this release is to provide GDPR compatible version of OpenMeetings

Room:
* Performance is improved
* Audio/Video streams were not closed in IE
* File conversion on Windows is improved

Other fixes and improvements, 9 issues were fixed

4.0.3
-----
[Release 4.0.3](https://archive.apache.org/dist/openmeetings/4.0.3), provides following improvements:

Security fix in Calendar

Room:
* Performance was improved
* Issues with audio/video were fixed
* Quick poll was added

Multiple improvements in web services

Other fixes and improvements, 13 issues were fixed

4.0.2
-----
[Release 4.0.2](https://archive.apache.org/dist/openmeetings/4.0.2), provides following improvements:

Security fixes in Chat and Admin

Chat:
* Send on Enter/Ctrl+Enter
* Invited guest's name displayed as expected
* Turned OFF global chat is not displayed
* Link works as expected
* Smiles works as expected
* Hover removed from chat

Room:
* Download as PDF
* Download/screen-sharing application in IE
* No duplicated users
* Activities&Actions improved
* Number of users is displayed in the room
* Mathematical formulas on WB

Other fixes and improvements, 32 issues were fixed

4.0.1
-----
[Release 4.0.1](https://archive.apache.org/dist/openmeetings/4.0.1), provides following improvements:

* Openlaszlo code is removed
* Login via OAuth is improved
* External video source is room is fixed
* Multiple improvements of White-board
* Multiple improvements of Chat
* JS/CSS files are minified and merged to reduce load time
* Overall stability is improved

Other fixes and improvements, 43 issues were fixed

4.0.0
-----
[Release 4.0.0](https://archive.apache.org/dist/openmeetings/4.0.0), provides following improvements:

* Room White board is rewritten to use HTML5 instead of Flash
* All Audio/Video components were rewritten using Apache Flex
* Bunch of automatic tests were written, code was cleaned-up and simplified
* outdated SMSlib was removed from the dependencies
* RTL in room is improved
* swftool 3rd party tool is not required any more
* OAuth authorization is fixed additional VK provider is added
* language resources are minimized
* performance is improved

Admin->Config
* config keys are generalized
* config types are introduced

Other fixes and improvements, 515 issues were fixed

3.3.2
-----
[Release 3.3.2](https://archive.apache.org/dist/openmeetings/3.3.2), provides following improvements:

* Audio/Video in conference room is fixed
* Strong password is enforced during self registration
* 'dashboard.show.chat' should work as expected
* New Setting is added 'user can create rooms'

Other fixes and improvements, 8 issues were fixed


3.3.1
-----
[Release 3.3.1](https://archive.apache.org/dist/openmeetings/3.3.1), provides following improvements:

* Clustering works as expected
* SIP works as expected
* Multiple issues in web services were fixed
* RTMPT mode is fixed
* Multiple UI improvements

Other fixes and improvements, 19 issues were fixed


3.3.0
-----
[Release 3.3.0](https://archive.apache.org/dist/openmeetings/3.3.0), provides following improvements:

Security fixes in:
* Chat
* All requests via security headers
* More secure password processing rules and storage
* More strict rules for uploaded files
* SQL injection in web services

11 security vulnerabilities were addressed

Whiteboard:
* Room is displayed without overlap in IE
* Multiple display issues
* Wb room element can now be hidden

Other fixes and improvements, 21 issues were fixed


3.2.1
-----
[Service release 1 for 3.2.0](https://archive.apache.org/dist/openmeetings/3.2.1), provides following improvements:

Room
* Video is more stable
* Office files download is fixed
* Multi-upload is added
* External video works as expected
* WB drawing on slides works as expected

Chat
* chat is made resizable
* multiple issues in chat are fixed
* typing indicator is added

Calendar
* date/time validator is improved
* whole group can be invited by admin to event

Other fixes and improvements, 49 issues were fixed

</details>



### 许可证
Apache OpenMeetings 在 Apache License 2.0 许可下发布。更多详情，请参阅 [LICENSE](http://www.apache.org/licenses/LICENSE-2.0)。

本产品还包含第三方软件。更多信息请查看 [NOTICE.md](/NOTICE.md)。

> **中文备注**：Apache License 2.0 是一个宽松的开源许可证，允许在商业环境中使用、修改和分发软件。
