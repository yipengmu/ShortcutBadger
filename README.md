项目介绍:

1.适配 不同厂商的Rom，如果rom本身不支持，则跳过该类launcher.

2.MIUI 默认的mipush-sdk会和自己的notifycation进行消息绑定，所以MIUI保留原生效果

3.调用方式：

`ShortcutBadger.setBadge(context, count);`

`ShortcutBadger.remove(context);`

注意事项：

1.badger为各厂商的launcher的现实逻辑，对于开发者只能通过系统暴漏的接口进行数据层面的传递。

2.另外，badger数不随着应用的卸载而更新，所以默认会在进程被干掉的时候，对badger进行清0

ShortcutBadger: [![Maven Central](https://maven-badges.herokuapp.com/maven-central/me.leolin/ShortcutBadger/badge.svg)](https://maven-badges.herokuapp.com/maven-central/me.leolin/ShortcutBadger)
===================================

The ShortcutBadger makes your Android App show the count of unread messages as a badge on your App shortcut!

# Support launchers:<br/>

<table>
<tr>
        <td width="130">
                <h3>Sony</h3>
                <br>
                <img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_sony.png"/>
        </td>
        <td width="130">
                <h3>Samsung</h3>
                <br>
                <img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_samsung.png"/>
        </td>
        <td width="130">
                <h3>LG</h3>
                <br>
                <img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_lg.png"/>
        </td>
        <td width="130">
                <h3>HTC</h3>
                <br>
                <img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_htc.png"/>
        </td>
</tr>
<tr>        
        <td width="130">
                <h3>Xiaomi</h3>
                <br>
                <img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_xiaomi.png"/>
        </td>
        <td width="130">
                <h3>ASUS</h3>
                <br>
                <img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_asus.png"/>
        </td>
        <td width="130">
                <h3>ADW</h3>
                <br>
                <img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_adw.png"/>
        </td>
        <td width="130">
                <h3>APEX</h3>
                <br>
                <img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_apex.png"/>
        </td>
<tr>        
        <td width="130">
                <h3>NOVA</h3>
                <br>
                <img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_nova.png"/>
        </td>
</tr>

<tr>
<td width="130">
<h3>Android</h3>
<h5>(before 4.4)</h5>
<h5>(Deprecated since 1.1.0)</h5>
<br>
<img src="https://raw.github.com/leolin310148/ShortcutBadger/master/screenshots/ss_android.png"/>
</td>
</tr>

</table> 


Nova launcher with TeslaUnread,Apex launcher,Adw Launcher provided by [notz](https://github.com/notz)</br/>
Solid launcher provided by [MajeurAndroid](https://github.com/MajeurAndroid)


USAGE
===================================
<br/>1. Add mavenCentral to your build script.

        repositories {
            mavenCentral()
        }
    
<br/>2. Add dependencies for ShortcutBadger, it's available from maven now.
        
        dependencies {
            compile 'me.leolin:ShortcutBadger:1.1.3@aar'
        }

<br/>3. Add the codes below:

        int badgeCount = 1;
        ShortcutBadger.with(getApplicationContext()).count(badgeCount);
        
<br/>4. If you want to remove the badge
        
        ShortcutBadger.with(getApplicationContext()).remove();
or
        
        ShortcutBadger.with(getApplicationContext()).count(0);
<br/>
<br/>
<br/>
<br/>


DEVELOP BY
===================================
[Leo Lin](https://github.com/leolin310148) - leolin310148@gmail.com


ABOUT Google Play Developer Term Violation
===================================
If you receive mail from Google contains message like :<br/> 

        REASON FOR WARNING: Violation of section 4.4 of the Developer Distribution Agreement.
        
Please use version 1.1.0+



CHANGE LOG
===================================
1.1.3:<br/>
Deprecate SamsungBadger and LGBadger, those devices can use DefaultBadger<br/>
<br/>

1.1.2:<br/>
Add support for 'com.miui.mihome2'<br/>
<br/>

1.1.1:<br/>
Add DefaultBadger because some launchers use android.intent.action.BADGE_COUNT_UPDATE to update count.
<br/>
Since the ShortcutBadgerException is helpless. So change api to set badge and never have to handle the exception again. 
<br/>
<br/>

1.1.0:<br/>
Remove Android Launcher support due to  Google Play Developer Term Violation since 4.4 
<br/>
<br/>

1.0.10:<br/>
Add Asus launcher support.
<br/>
<br/>

1.0.9:<br/>
Add xiaomi launcher support.


LICENSE
===================================
<br/>
        
        Copyright 2014 Leo Lin
        
        Licensed under the Apache License, Version 2.0 (the "License");
        you may not use this file except in compliance with the License.
        You may obtain a copy of the License at
        
            http://www.apache.org/licenses/LICENSE-2.0
        
        Unless required by applicable law or agreed to in writing, software
        distributed under the License is distributed on an "AS IS" BASIS,
        WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
        See the License for the specific language governing permissions and
        limitations under the License.
<br/>       
