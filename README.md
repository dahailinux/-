# 服务器不出网后还存在的威胁
服务器配置不出网后还存在的威胁

![image](https://github.com/dahailinux/-/assets/54297681/80fabc9b-bfc5-4071-b98b-2a087cc14d6f)

服务器不允许出网后还有啥威胁											
内部人员直接拖库			内应直接拖库					前端xss控制客服浏览器，直接偷用户数据			
dns隧道			内应联合黑客，留出通道，使黑客可以渗入内网；					开发人员主动写个漏洞上去，然后就配合黑客做远控，从而渗入到机房			
ping隧道			机房物理安全/人为安全					里应外合是重点防御的，内部人员有一个特殊权限或自己修改了一下，配合外面黑客就攻击进来了。安全要深入到每一个大家都觉得不可能的点，那很多安全事故的根源。对特例机器要重点监控			
内网作为跳板控制服务器			机房有一台能出外网的，就可以做代理渗入内网；					供应链攻击，使用被嵌马的系统或应用或docker镜像；			
xss注入			所有对外的应用程序ftp/ldap等都可能有漏洞被利用后执行rce								
sql注入			机房保护得好，也开了白名单，白名单机器被黑掉了，会有大影响，所以要做好安全监控；								
rce后获取机房IP			对有前端代码的服务器进行rce，因为这台机器一定对外；								
网络安全设备有0day，直接可以进入内网，偷资料后，传出去；			通过堡垒机漏洞或horizon等中转的机器的漏洞，实现远控，从而使机房沦陷								
rce后，偷走资料			通过应用漏洞远控内网服务器，从而攻入到机房服务器因为有白名单								
webshell			勒索病毒								
