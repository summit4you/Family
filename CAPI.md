Family
=====
版本：0.1  
作者：[丘文峰](mailto:809104518@qq.com)

本文档用于描述Family的客户端接口
******************************
索引
----
* 下行接口
	*	[好友动态列表接口](#好友动态列表接口)
	*	[全部打赌列表接口](#全站动态列表接口)
	*	[通知列表接口](#通知列表接口)
	*	[私信列表接口](#私信列表接口)
	*	[私信详情](#私信详情)
	*	[获取家人接口](#获取家人接口)
	*	[我的个人信息](#我的个人信息)
	*	[相册列表](#相册列表)
	*	[相册图片列表](#相册图片列表)
	*	[个人封面](#个人封面)
	*	[图片详情](#图片详情)
	*	[评论列表](#评论列表)


* 上行接口
	*	[登录](#登录)
	*	[撰写评论](#撰写评论)
	*	[转载](#转载)
	*	[表态](#表态)
	*	[退出](#退出)
	*	[获取注册验证码](#获取注册验证码)
	*	[注册](#注册)
	*	[单向加家人](#单向加家人)
	*	[通过家人验证](#通过家人验证)
	*	[上传图片](#上传图片)
	*	[发布图片](#发布图片)
	*	[发布日记](#发布日记)
	*	[发布视频](#发布视频)
	*	[发布私信](#发布私信)
	*	[创建成长相册](#创建成长相册)
	*	[更改封面](#更改封面)
	*	[更改头像](#更改头像)
	*	[更改昵称](#更改昵称)
	*	[编写心情](#编写心情)
	*	[邀请好友](#邀请好友)
	

接口说明
--------



******************************

<h2>登录</h2>
域名/capi/do.php?ac=login&username=summit&password=likeyou&loginsubmit=true
#### 请求参数
	* 用户名 -- username
	* 密码 -- password
	* 提交类型 -- loginsubmit， 必须为true
#### 返回字段
	* 错误码 -- code, 0:代表成功， 1:代表失败
	* 错误类型 -- action, login_success:代表登录成功
	* 错误信息 -- msg, 详细参见附录
	* API密钥 -- m_auth, 每次调用接口，需要提供此key以验证用户
	* 用户空间信息 -- space
		* groupid -- 所在用户组（级别）
		* credit -- 金币
		* experience -- 经验
		* username -- 用户名
		* name -- 实名
		* namestatus -- 是否实名
		* videostatus -- 是否视频认证
		* friendnum -- 好友数
		* feedfriendnum -- 粉丝数
		* viewnum -- 浏览次数
		* notenum -- 通知数
		* addfriendnum -- 关注数
		* doingnum -- 心情数
		* lastpost -- 最新提交时间
		* lastlogin -- 最新登录时间
		* attachsize -- 空间大小
		* flag -- 是否被禁
		* newpm -- 是否有新通知
		* avatar -- 个人头像
		* photonum -- 相片数
		* videonum -- 视频数
		* albumnum -- 相册数
		* reward -- 操作增加的金币分和经验
			* credit -- 金币
			* experience -- 经验
#### 样例
	{
	    "code": {
	        "space": {
	            "uid": "5",
	            "groupid": "5",
	            "credit": "40",
	            "experience": "30",
	            "username": "13751341409",
	            "name": "",
	            "namestatus": "0",
	            "videostatus": "0",
	            "shopstatus": "0",
	            "domain": "",
	            "friendnum": "0",
	            "feedfriendnum": "0",
	            "viewnum": "0",
	            "notenum": "0",
	            "addfriendnum": "0",
	            "mtaginvitenum": "0",
	            "eventinvitenum": "0",
	            "myinvitenum": "0",
	            "pokenum": "0",
	            "doingnum": "0",
	            "blognum": "0",
	            "goodsnum": "0",
	            "couponsnum": "0",
	            "photonum": "0",
	            "videonum": "0",
	            "disclosenum": "0",
	            "albumnum": "0",
	            "threadnum": "0",
	            "pollnum": "0",
	            "eventnum": "0",
	            "sharenum": "0",
	            "lovenum": "0",
	            "dateline": "1347024667",
	            "updatetime": "0",
	            "lastsearch": "0",
	            "lastpost": "0",
	            "lastlogin": "1347535420",
	            "lastsend": "0",
	            "attachsize": "0",
	            "addsize": "0",
	            "addfriend": "0",
	            "flag": "0",
	            "newpm": "0",
	            "avatar": "0",
	            "regip": "125.90.59.196",
	            "ip": "127000000",
	            "mood": "0",
	            "referrals": "0",
	            "reward": {
	                "credit": 0,
	                "experience": 0
	            }
	        },
	        "m_auth": "9136fbT%2BdF87hKneldWrV%2BFJmNTxca2%2FyzNWCenpFZfATrpxXtJvpaXCJ5lQ5Qh5ryfPzm7JTChrwaCqgvGM"
	    },
	    "data": [],
	    "msg": "登录成功了，现在引导您进入登录前页面 \\1",
	    "action": "login_success"
	}
[↑返回顶部](#Family)