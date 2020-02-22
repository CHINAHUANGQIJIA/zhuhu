<template>
	<div>
		<div class="nav gutter">
			<div class="nav-bar" >
					<ul class="nav-list flex-left">
						<svg xmlns="http://www.w3.org/2000/svg" class="Icon ZhihuLogo ZhihuLogo--blue Icon--logo" aria-hidden="true" style="width: 64px; height: 30px;" viewBox="0 0 200 91" width="64" height="30"><title /><g><path fill-rule="evenodd" d="M 53.29 80.035 l 7.32 0.002 l 2.41 8.24 l 13.128 -8.24 h 15.477 v -67.98 H 53.29 v 67.978 Z m 7.79 -60.598 h 22.756 v 53.22 h -8.73 l -8.718 5.473 l -1.587 -5.46 l -3.72 -0.012 v -53.22 Z M 46.818 43.162 h -16.35 c 0.545 -8.467 0.687 -16.12 0.687 -22.955 h 15.987 s 0.615 -7.05 -2.68 -6.97 H 16.807 c 1.09 -4.1 2.46 -8.332 4.1 -12.708 c 0 0 -7.523 0 -10.085 6.74 c -1.06 2.78 -4.128 13.48 -9.592 24.41 c 1.84 -0.2 7.927 -0.37 11.512 -6.94 c 0.66 -1.84 0.785 -2.08 1.605 -4.54 h 9.02 c 0 3.28 -0.374 20.9 -0.526 22.95 H 6.51 c -3.67 0 -4.863 7.38 -4.863 7.38 H 22.14 C 20.765 66.11 13.385 79.24 0 89.62 c 6.403 1.828 12.784 -0.29 15.937 -3.094 c 0 0 7.182 -6.53 11.12 -21.64 L 43.92 85.18 s 2.473 -8.402 -0.388 -12.496 c -2.37 -2.788 -8.768 -10.33 -11.496 -13.064 l -4.57 3.627 c 1.363 -4.368 2.183 -8.61 2.46 -12.71 H 49.19 s -0.027 -7.38 -2.372 -7.38 Z m 128.752 -0.502 c 6.51 -8.013 14.054 -18.302 14.054 -18.302 s -5.827 -4.625 -8.556 -1.27 c -1.874 2.548 -11.51 15.063 -11.51 15.063 l 6.012 4.51 Z m -46.903 -18.462 c -2.814 -2.577 -8.096 0.667 -8.096 0.667 s 12.35 17.2 12.85 17.953 l 6.08 -4.29 s -8.02 -11.752 -10.83 -14.33 Z M 199.99 46.5 c -6.18 0 -40.908 0.292 -40.953 0.292 v -31.56 c 1.503 0 3.882 -0.124 7.14 -0.376 c 12.773 -0.753 21.914 -1.25 27.427 -1.504 c 0 0 3.817 -8.496 -0.185 -10.45 c -0.96 -0.37 -7.24 1.43 -7.24 1.43 s -51.63 5.153 -72.61 5.64 c 0.5 2.756 2.38 5.336 4.93 6.11 c 4.16 1.087 7.09 0.53 15.36 0.277 c 7.76 -0.5 13.65 -0.76 17.66 -0.76 v 31.19 h -41.71 s 0.88 6.97 7.97 7.14 h 33.73 v 22.16 c 0 4.364 -3.498 6.87 -7.65 6.6 c -4.4 0.034 -8.15 -0.36 -13.027 -0.566 c 0.623 1.24 1.977 4.496 6.035 6.824 c 3.087 1.502 5.054 2.053 8.13 2.053 c 9.237 0 14.27 -5.4 14.027 -14.16 V 53.93 h 38.235 c 3.026 0 2.72 -7.432 2.72 -7.432 Z" /></g></svg>
						<ul class="Tabs AppHeader-Tabs" role="navigation">
							<li class="Tabs-item AppHeader-Tab Tabs-item--noMeta" role="tab">
								<router-link to="/home" class="Tabs-link AppHeader-TabsLink is-active" >首页</router-link></li>
								<li class="Tabs-item AppHeader-Tab Tabs-item--noMeta" role="tab">
									<router-link to="/explore" class="Tabs-link AppHeader-TabsLink is-active" >发现</router-link></li>
									<li class="Tabs-item AppHeader-Tab Tabs-item--noMeta" role="tab">
									<router-link to="/question/waiting" class="Tabs-link AppHeader-TabsLink is-active" >等你来答</router-link></li></ul>
							<div class="serach  flex flex-around">
								<div class="search-t">
									<input type="text">
								</div>
								<div class="search-b">
									<input type="button" value="提问">
								</div>
								<div class="AppHeader-userInfo"><div class="Popover PushNotifications AppHeader-notifications"><button type="button" id="Popover7-toggle" aria-haspopup="true" aria-expanded="false" aria-owns="Popover7-content" class="Button PushNotifications-icon Button--plain"><span style="display: inline-flex; align-items: center;">​<svg class="Zi Zi--Bell" fill="currentColor" viewBox="0 0 24 24" width="22" height="22"><path d="M4.523 15.076l.804-6.757a6.753 6.753 0 0 1 4.945-5.7 1.823 1.823 0 0 1 3.623 0 6.753 6.753 0 0 1 4.945 5.7l.804 6.757a2.293 2.293 0 0 0 1.712 2.108 1.093 1.093 0 0 1-.297 2.15H3.108a1.093 1.093 0 0 1-.297-2.15 2.293 2.293 0 0 0 1.712-2.108zM12.083 23a2.758 2.758 0 0 1-2.753-2.509.229.229 0 0 1 .232-.24h5.043a.229.229 0 0 1 .232.24 2.759 2.759 0 0 1-2.753 2.51z"></path></svg></span><span class="PushNotifications-count">8</span></button></div><div><div class="Popover Messages AppHeader-messages"><button type="button" id="Popover8-toggle" aria-haspopup="true" aria-expanded="false" aria-owns="Popover8-content" class="Button Messages-icon Button--plain"><span style="display: inline-flex; align-items: center;">​<svg class="Zi Zi--Comments" fill="currentColor" viewBox="0 0 24 24" width="22" height="22"><path d="M11 2c5.571 0 9 4.335 9 8 0 6-6.475 9.764-11.481 8.022-.315-.07-.379-.124-.78.078-1.455.54-2.413.921-3.525 1.122-.483.087-.916-.25-.588-.581 0 0 .677-.417.842-1.904.064-.351-.14-.879-.454-1.171A8.833 8.833 0 0 1 2 10c0-3.87 3.394-8 9-8zm10.14 9.628c.758.988.86 2.009.86 3.15 0 1.195-.619 3.11-1.368 3.938-.209.23-.354.467-.308.722.12 1.073.614 1.501.614 1.501.237.239-.188.562-.537.5-.803-.146-1.495-.42-2.546-.811-.29-.146-.336-.106-.563-.057-2.043.711-4.398.475-6.083-.927 5.965-.524 8.727-3.03 9.93-8.016z" fill-rule="evenodd"></path></svg></span></button></div></div><div class="AppHeader-profile"><div class="Popover AppHeader-menu"><button type="button" id="Popover9-toggle" aria-haspopup="true" aria-expanded="false" aria-owns="Popover9-content" class="Button AppHeader-profileEntry Button--plain"><img class="Avatar AppHeader-profileAvatar" width="30" height="30" src="https://pic1.zhimg.com/v2-bb75c593f8f5eabdaca6be100c0c3076_is.jpg" srcset="https://pic1.zhimg.com/v2-bb75c593f8f5eabdaca6be100c0c3076_im.jpg 2x"></button></div><div class="Popover AppHeaderProfileMenu-creatorHintPopover"><div class="AppHeaderProfileMenu-creatorHintToggler" id="Popover10-toggle" aria-haspopup="true" aria-expanded="false" aria-owns="Popover10-content"></div></div></div></div>
							</div>
						</li>
						
						
					</ul>				
			</div>
		</div>
		<router-view />
		
	</div>
</template>

<script>
export default{
	name:'nav',
	data(){
		return {};
	},
	created() {}
};
</script>

<style lang="scss" scoped>
	.ZhihuLogo {
	    fill: #0084ff;
	}

	.AppHeader-Tabs {
	    border-bottom: none;
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: flex;
	    margin: 0 23px;
	}
	.router-link-active {
	    color: #444;
	}

ol, ul {
    padding: 0;
    margin: 0;
}
.AppHeader-Tab {
    padding: 0 17px;
}
.Tabs-item {
    display: inline-block;
   
}
.AppHeader-TabsLink {
    color: #8590a6;
    font-size: 15px;
}

.Tabs-link {
    position: relative;
    display: inline-block;
    padding: 14px 0;
    font-size: 16px;
    line-height: 22px;
    color: #1a1a1a;
    text-align: center;
}


.AppHeader-TabsLink {
    color: #8590a6;
    font-size: 15px;
}



.router-link-active {
    
    font-weight: 600;
    color: black;
    font-synthesis: style;
    border-bottom: 2px solid rgb(0,132,255);
    content: "";
}

	.gutter{
		position: relative;
		margin-bottom: 10px;
		 border: 1px solid #e9e9e9;
		    box-shadow: 0 0 6px #e4e4e4;
		
	}
	.nav-bar{
		
	}
	.search-t {
	   input{
		  position: relative;
		  display: flex;
		  -webkit-box-align: center;
		  align-items: center;
		  height: 34px;
		  padding: 4px 10px;
		  font-size: 14px;
		  border: 1px solid #ebebeb;
		  border-radius: 3px;
		  box-sizing: border-box;
		  width: 326px;
		  transition: width .2s ease,background .3s ease;
		  background: #f6f6f6;
	   }
	}
	.search-b {
		input{
			font-size: 18px;
			text-align: center;
			border: 1px solid;
			border-radius: 3px;
			border-color: #0084ff;
			transition: opacity .3s ease,transform .3s ease,-webkit-transform .3s ease;
			height: 34px;
			width: 60px;
			margin-left: 20px;
			color: #fff;
			background-color: #0084ff;
		}
	}
	
	.AppHeader-userInfo {
			margin-left: 120px;
	    -webkit-box-flex: 1;
	    -ms-flex: 1 1;
	    flex: 1 1;
	    -webkit-box-pack: end;
	    -ms-flex-pack: end;
	    justify-content: flex-end;
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: flex;
	    -webkit-box-align: center;
	    -ms-flex-align: center;
	    align-items: center;
	}
.AppHeader-messages, .AppHeader-notifications {

    margin-right: 30px;
}
.Popover {
    position: relative;
    display: inline-block;
}
.Button--link, .Button--plain {
    height: auto;
    padding: 0;
    line-height: inherit;
    background-color: transparent;
    border: none;
    border-radius: 0;
}


.AppHeader-profile {
    position: relative;
}
.AppHeader-profileAvatar {
    vertical-align: top;
}
.Avatar {
    background: #fff;
    border-radius: 2px;

}
.AppHeaderProfileMenu-creatorHintPopover {
    position: absolute;
    right: 0px;
    top: 0px;
    z-index: -1;
}
.Button {
 
    color: #8590a6;
    
}


</style>
