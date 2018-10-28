---
name: linux下如何切换到root用户
about: Describe this issue template's purpose here.

---

默认安装完成之后并不知道root用户的密码，那么如何应用root权限呢？
(1)sudo 命令
blackrosie@blackrosie-ThinkPad-X240:$ sudo
(2)sudo -i
blackrosie@blackrosie-ThinkPad-X240:$ sudo -i
通过这种方法输入当前管理员用户的密码就可以进到root用户
root@blackrosie-ThinkPad-X240:#
(3)如果想一直使用root权限，要通过su切换到root用户。
那我们首先要重设置root用户的密码：
root@blackrosie-ThinkPad-X240:# sudo passwd root
输入新的 UNIX 密码：
重新输入新的 UNIX 密码：
passwd：已成功更新密码
root@blackrosie-ThinkPad-X240:#
(4)之后就可以自由的切换到root用户了
root@blackrosie-ThinkPad-X240:# su
root@blackrosie-ThinkPad-X240:# su "king"
没有用户“king”的密码项
root@blackrosie-ThinkPad-X240:# exit
exit
root@blackrosie-ThinkPad-X240:~#
