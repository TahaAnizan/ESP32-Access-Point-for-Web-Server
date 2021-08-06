# ESP32-Access-Point-for-Web-Server
<!DOCTYPE html>
<!-- saved from url=(0065)https://randomnerdtutorials.com/esp32-access-point-ap-web-server/ -->
<html lang="en-US" prefix="og: https://ogp.me/ns#"><link type="text/css" rel="stylesheet" id="dark-mode-custom-link"><link type="text/css" rel="stylesheet" id="dark-mode-general-link"><style lang="en" type="text/css" id="dark-mode-custom-style"></style><style lang="en" type="text/css" id="dark-mode-native-style"></style><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
	
	<link rel="profile" href="https://gmpg.org/xfn/11">
	<title>ESP32 Access Point (AP) for Web Server | Random Nerd Tutorials</title><link rel="preload" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/esp32-web-server-arduino-ide-parts-required.jpg" as="image" srcset="https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-web-server-arduino-ide-parts-required.jpg?w=750&amp;quality=100&amp;strip=all&amp;ssl=1 750w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-web-server-arduino-ide-parts-required.jpg?resize=300%2C200&amp;quality=100&amp;strip=all&amp;ssl=1 300w" sizes="(max-width: 750px) 100vw, 750px"><link rel="preload" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/access-point.png" as="image" srcset="https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/access-point.png?w=800&amp;quality=100&amp;strip=all&amp;ssl=1 800w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/access-point.png?resize=300%2C176&amp;quality=100&amp;strip=all&amp;ssl=1 300w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/access-point.png?resize=768%2C451&amp;quality=100&amp;strip=all&amp;ssl=1 768w" sizes="(max-width: 800px) 100vw, 800px"><link rel="preload" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/esp32-station.png" as="image" srcset="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-station.png?w=900&amp;quality=100&amp;strip=all&amp;ssl=1 900w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-station.png?resize=300%2C151&amp;quality=100&amp;strip=all&amp;ssl=1 300w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-station.png?resize=768%2C386&amp;quality=100&amp;strip=all&amp;ssl=1 768w" sizes="(max-width: 828px) 100vw, 828px"><link rel="preload" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/ESP32-access-point-1.jpg" as="image" srcset="https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg?w=1280&amp;quality=100&amp;strip=all&amp;ssl=1 1280w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg?resize=300%2C169&amp;quality=100&amp;strip=all&amp;ssl=1 300w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg?resize=768%2C432&amp;quality=100&amp;strip=all&amp;ssl=1 768w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg?resize=1024%2C576&amp;quality=100&amp;strip=all&amp;ssl=1 1024w" sizes="(max-width: 828px) 100vw, 828px"><link rel="preload" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/logornt.png" as="image" srcset="" sizes=""><style id="flying-press-css">@charset "UTF-8";.wp-block-image{margin-bottom:1em}.wp-block-image img{max-width:100%}.wp-block-image:not(.is-style-rounded) img{border-radius:inherit}.wp-block-image .aligncenter{display:table}.wp-block-image .aligncenter{margin-left:auto;margin-right:auto}.wp-block-navigation:not(.has-background) .wp-block-navigation__container .wp-block-navigation__container{color:#1e1e1e;background-color:#fff;min-width:200px}.wp-block-navigation-link{display:flex;align-items:center;position:relative;margin:0}.wp-block-navigation-link .wp-block-navigation__container:empty{display:none}.wp-block-navigation__container{list-style:none;margin:0;padding-left:0;display:flex;flex-wrap:wrap}.is-vertical .wp-block-navigation__container{display:block}.has-child>.wp-block-navigation-link__content{padding-right:.5em}.has-child .wp-block-navigation__container{border:1px solid rgba(0,0,0,.15);background-color:inherit;color:inherit;position:absolute;left:0;top:100%;width:-webkit-fit-content;width:-moz-fit-content;width:fit-content;z-index:2;opacity:0;transition:opacity .1s linear;visibility:hidden}.has-child .wp-block-navigation__container>.wp-block-navigation-link>.wp-block-navigation-link__content{flex-grow:1}.has-child .wp-block-navigation__container>.wp-block-navigation-link>.wp-block-navigation-link__submenu-icon{padding-right:.5em}@media (min-width:782px){.has-child .wp-block-navigation__container{left:1.5em}.has-child .wp-block-navigation__container .wp-block-navigation__container{left:100%;top:-1px}.has-child .wp-block-navigation__container .wp-block-navigation__container:before{content:"";position:absolute;right:100%;height:100%;display:block;width:.5em;background:0 0}.has-child .wp-block-navigation__container .wp-block-navigation-link__submenu-icon svg{transform:rotate(0)}}.has-child:hover>.wp-block-navigation__container{visibility:visible;opacity:1;display:flex;flex-direction:column}.has-child:focus-within>.wp-block-navigation__container{visibility:visible;opacity:1;display:flex;flex-direction:column}.wp-block-navigation[style*=text-decoration] .wp-block-navigation-link,.wp-block-navigation[style*=text-decoration] .wp-block-navigation-link__content,.wp-block-navigation[style*=text-decoration] .wp-block-navigation-link__content:active,.wp-block-navigation[style*=text-decoration] .wp-block-navigation-link__content:focus,.wp-block-navigation[style*=text-decoration] .wp-block-navigation__container{text-decoration:inherit}.wp-block-navigation:not([style*=text-decoration]) .wp-block-navigation-link__content,.wp-block-navigation:not([style*=text-decoration]) .wp-block-navigation-link__content:active,.wp-block-navigation:not([style*=text-decoration]) .wp-block-navigation-link__content:focus{text-decoration:none}.wp-block-navigation-link__content{color:inherit;padding:.5em 1em}.wp-block-navigation-link__content+.wp-block-navigation-link__content{padding-top:0}.has-text-color .wp-block-navigation-link__content{color:inherit}.wp-block-navigation-link__label{word-break:normal;overflow-wrap:break-word}.wp-block-navigation-link__submenu-icon{height:inherit;padding:.375em 1em .375em 0}.wp-block-navigation-link__submenu-icon svg{fill:currentColor}@media (min-width:782px){.wp-block-navigation-link__submenu-icon svg{transform:rotate(90deg)}}.has-text-align-center{text-align:center}.aligncenter{clear:both}.grid-15:after,.grid-15:before,.grid-25:after,.grid-25:before,.grid-60:after,.grid-60:before,.grid-container:after,.grid-container:before,[class*=mobile-grid-]:after,[class*=mobile-grid-]:before,[class*=tablet-grid-]:after,[class*=tablet-grid-]:before{content:".";display:block;overflow:hidden;visibility:hidden;font-size:0;line-height:0;width:0;height:0}.grid-15:after,.grid-25:after,.grid-60:after,.grid-container:after,[class*=mobile-grid-]:after,[class*=tablet-grid-]:after{clear:both}.grid-container{margin-left:auto;margin-right:auto;max-width:1200px;padding-left:10px;padding-right:10px}.grid-15,.grid-25,.grid-60,[class*=mobile-grid-],[class*=tablet-grid-]{box-sizing:border-box;padding-left:10px;padding-right:10px}.grid-parent{padding-left:0;padding-right:0}@media (max-width:767px){.mobile-grid-100{clear:both;width:100%}}@media (min-width:768px) and (max-width:1024px){[class*=tablet-pull-],[class*=tablet-push-]{position:relative}.tablet-grid-15{float:left;width:15%}.tablet-push-15{left:15%}.tablet-grid-25{float:left;width:25%}.tablet-grid-60{float:left;width:60%}.tablet-pull-60{left:-60%}}@media (min-width:1025px){.pull-60,.push-15{position:relative}.grid-15{float:left;width:15%}.push-15{left:15%}.grid-25{float:left;width:25%}.grid-60{float:left;width:60%}.pull-60{left:-60%}}a,body,div,em,form,h1,h2,html,iframe,label,li,p,span,strong,ul{border:0;margin:0;padding:0}html{font-family:sans-serif;-webkit-text-size-adjust:100%;-ms-text-size-adjust:100%}article,aside,figure,header,main,nav,section{display:block}ul{list-style:none}a{background-color:transparent}a img{border:0}body,button,input{font-family:-apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";font-weight:400;text-transform:none;font-size:17px;line-height:1.5}p{margin-bottom:1.5em}h1,h2{font-family:inherit;font-size:100%;font-style:inherit;font-weight:inherit}h1{font-size:42px;margin-bottom:20px;line-height:1.2em;font-weight:400;text-transform:none}h2{font-size:35px;margin-bottom:20px;line-height:1.2em;font-weight:400;text-transform:none}ul{margin:0 0 1.5em 3em}ul{list-style:disc}li>ul{margin-bottom:0;margin-left:1.5em}strong{font-weight:700}em{font-style:italic}figure{margin:0}img{height:auto;max-width:100%}button,input{font-size:100%;margin:0;vertical-align:baseline}button{border:1px solid transparent;background:#55555e;cursor:pointer;-webkit-appearance:button;padding:10px 20px;color:#fff}input[type=search]{-webkit-appearance:textfield;box-sizing:content-box}input[type=search]::-webkit-search-decoration{-webkit-appearance:none}button::-moz-focus-inner,input::-moz-focus-inner{border:0;padding:0}input[type=email],input[type=search]{background:#fafafa;color:#666;border:1px solid #ccc;border-radius:0;padding:10px 15px;box-sizing:border-box;max-width:100%}a,button,input{transition:color .1s ease-in-out,background-color .1s ease-in-out}a,a:focus,a:hover,a:visited{text-decoration:none}.aligncenter{clear:both;display:block;margin:0 auto}.no-sidebar .entry-content .alignfull{margin-left:calc(-100vw/2 + 100%/2);margin-right:calc(-100vw/2 + 100%/2);max-width:100vw;width:auto}.screen-reader-text{border:0;clip:rect(1px,1px,1px,1px);-webkit-clip-path:inset(50%);clip-path:inset(50%);height:1px;margin:-1px;overflow:hidden;padding:0;position:absolute!important;width:1px;word-wrap:normal!important}.screen-reader-text:focus{background-color:#f1f1f1;border-radius:3px;box-shadow:0 0 2px 2px rgba(0,0,0,.6);clip:auto!important;-webkit-clip-path:none;clip-path:none;color:#21759b;display:block;font-size:.875rem;font-weight:700;height:auto;left:5px;line-height:normal;padding:15px 23px 14px;text-decoration:none;top:5px;width:auto;z-index:100000}.entry-content:after,.inside-footer-widgets:not(.grid-container):after,.inside-header:not(.grid-container):after,.inside-navigation:not(.grid-container):after,.inside-top-bar:not(.grid-container):after,.paging-navigation:after,.site-content:after,.site-header:after{content:"";display:table;clear:both}.main-navigation{z-index:100;padding:0;clear:both;display:block}.main-navigation a{display:block;text-decoration:none;font-weight:400;text-transform:none;font-size:15px}.main-navigation ul{list-style:none;margin:0;padding-left:0}.main-navigation .main-nav ul li a{padding-left:20px;padding-right:20px;line-height:60px}.inside-navigation{position:relative}.main-navigation li{float:left;position:relative}.nav-float-right .inside-header .main-navigation{float:right;clear:right}.nav-float-left .inside-header .main-navigation{float:left;clear:left}.nav-aligned-center .main-navigation:not(.toggled) .menu>li,.nav-aligned-right .main-navigation:not(.toggled) .menu>li{float:none;display:inline-block}.nav-aligned-center .main-navigation:not(.toggled) ul,.nav-aligned-right .main-navigation:not(.toggled) ul{letter-spacing:-.31em;font-size:1em}.nav-aligned-center .main-navigation:not(.toggled) ul li,.nav-aligned-right .main-navigation:not(.toggled) ul li{letter-spacing:normal}.nav-aligned-center .main-navigation{text-align:center}.nav-aligned-right .main-navigation{text-align:right}.main-navigation li.search-item{float:right}.main-navigation .mobile-bar-items a{padding-left:20px;padding-right:20px;line-height:60px}.main-navigation ul ul{display:block;box-shadow:1px 1px 0 rgba(0,0,0,.1);float:left;position:absolute;left:-99999px;opacity:0;z-index:99999;width:200px;text-align:left;top:auto;transition:opacity 80ms linear;transition-delay:0s;pointer-events:none;height:0;overflow:hidden}.main-navigation ul ul a{display:block}.main-navigation ul ul li{width:100%}.main-navigation .main-nav ul ul li a{line-height:normal;padding:10px 20px;font-size:14px}.main-navigation .main-nav ul li.menu-item-has-children>a{padding-right:0;position:relative}.main-navigation.sub-menu-left .sub-menu{right:0}.main-navigation:not(.toggled) ul li.sfHover>ul,.main-navigation:not(.toggled) ul li:hover>ul{left:auto;opacity:1;transition-delay:150ms;pointer-events:auto;height:auto;overflow:visible}.main-navigation:not(.toggled) ul ul li.sfHover>ul,.main-navigation:not(.toggled) ul ul li:hover>ul{left:100%;top:0}.main-navigation.sub-menu-left:not(.toggled) ul ul li.sfHover>ul,.main-navigation.sub-menu-left:not(.toggled) ul ul li:hover>ul{right:100%;left:auto}.nav-float-right .main-navigation ul ul ul{top:0}.menu-item-has-children .dropdown-menu-toggle{display:inline-block;height:100%;clear:both;padding-right:20px;padding-left:10px}nav ul ul .menu-item-has-children .dropdown-menu-toggle{float:right}.widget-area .main-navigation li{float:none;display:block;width:100%;padding:0;margin:0}.sidebar .main-navigation.sub-menu-right ul li.sfHover ul,.sidebar .main-navigation.sub-menu-right ul li:hover ul{top:0;left:100%}.sidebar .main-navigation.sub-menu-left ul li.sfHover ul,.sidebar .main-navigation.sub-menu-left ul li:hover ul{top:0;right:100%}.site-main .comment-navigation,.site-main .post-navigation,.site-main .posts-navigation{margin:0 0 2em;overflow:hidden}.site-main .post-navigation{margin-bottom:0}.paging-navigation .nav-next,.paging-navigation .nav-previous{display:none}.paging-navigation .nav-links>*{padding:0 5px}.paging-navigation .nav-links .current{font-weight:700}.nav-links>:first-child{padding-left:0}.site-header{position:relative}.inside-header{padding:20px 40px}.site-logo{display:inline-block;max-width:100%}.nav-float-right .header-widget{position:relative;top:-10px}.nav-float-right .header-widget .widget{padding:0 0 10px}.nav-float-left .inside-header .site-branding,.nav-float-left .inside-header .site-logo{float:right;clear:right}.nav-float-left .inside-header:after{clear:both;content:'';display:table}.nav-float-right .inside-header .site-branding{display:inline-block}.header-aligned-center .site-header{text-align:center}.entry-content:not(:first-child){margin-top:2em}.entry-header,.site-content{word-wrap:break-word}.entry-title{margin-bottom:0}.entry-content>p:last-child{margin-bottom:0}iframe{max-width:100%}.widget-area .widget{padding:40px}.sidebar .widget :last-child{margin-bottom:0}.widget{margin:0 0 30px;box-sizing:border-box}.separate-containers .widget:last-child,.widget:last-child{margin-bottom:0}.sidebar .widget{font-size:17px}.widget_nav_menu ul ul{margin-left:1em;margin-top:5px}.sidebar .grid-container{max-width:100%;width:100%}.post{margin:0 0 2em}.separate-containers .inside-article,.separate-containers .paging-navigation{padding:40px}.separate-containers .site-main>*,.separate-containers .widget{margin-bottom:20px}.separate-containers .site-main{margin:20px}.separate-containers.no-sidebar .site-main{margin-left:0;margin-right:0}.separate-containers .inside-left-sidebar,.separate-containers .inside-right-sidebar{margin-top:20px;margin-bottom:20px}.widget-area .main-navigation{margin-bottom:20px}.separate-containers .site-main>:last-child{margin-bottom:0}.full-width-content .container.grid-container{max-width:100%}.full-width-content.no-sidebar.separate-containers .site-main{margin:0}.footer-bar .widget_nav_menu>div>ul{display:inline-block;vertical-align:top}.footer-bar .widget_nav_menu li{margin:0 10px;float:left;padding:0}.footer-bar .widget_nav_menu li:first-child{margin-left:0}.footer-bar .widget_nav_menu li:last-child{margin-right:0}.footer-bar .widget_nav_menu li ul{display:none}.top-bar .widget_nav_menu li{margin:0 10px;float:left;padding:0}.top-bar .widget_nav_menu li:first-child{margin-left:0}.top-bar .widget_nav_menu li:last-child{margin-right:0}.top-bar .widget_nav_menu li ul{display:none}.top-bar .widget_nav_menu>div>ul{display:inline-block;vertical-align:top}nav.toggled .icon-arrow-left svg{transform:rotate(-90deg)}nav.toggled .icon-arrow-right svg{transform:rotate(90deg)}nav.toggled .sfHover>a>.dropdown-menu-toggle .gp-icon svg{transform:rotate(180deg)}nav.toggled .sfHover>a>.dropdown-menu-toggle .gp-icon.icon-arrow-left svg{transform:rotate(-270deg)}nav.toggled .sfHover>a>.dropdown-menu-toggle .gp-icon.icon-arrow-right svg{transform:rotate(270deg)}.container.grid-container{width:auto}.infinite-scroll .paging-navigation{display:none}.menu-toggle,.mobile-bar-items,.sidebar-nav-mobile{display:none}.menu-toggle{padding:0 20px;line-height:60px;margin:0;font-weight:400;text-transform:none;font-size:15px;cursor:pointer}button.menu-toggle{background-color:transparent;width:100%;border:0;text-align:center}button.menu-toggle:active,button.menu-toggle:focus,button.menu-toggle:hover{background-color:transparent}.menu-toggle .mobile-menu{padding-left:3px}.menu-toggle .mobile-menu:empty{display:none}.nav-search-enabled .main-navigation .menu-toggle{text-align:left}.mobile-bar-items{display:none;position:absolute;right:0;top:0;z-index:21;list-style-type:none}.mobile-bar-items a{display:inline-block}nav.toggled ul ul.sub-menu{width:100%}.dropdown-hover .main-navigation.toggled ul li.sfHover>ul,.dropdown-hover .main-navigation.toggled ul li:hover>ul{transition-delay:0s}.main-navigation.toggled ul ul{transition:0s;visibility:hidden}.main-navigation.toggled .main-nav>ul{display:block}.main-navigation.toggled .main-nav ul ul.toggled-on{position:relative;top:0;left:auto!important;right:auto!important;width:100%;pointer-events:auto;height:auto;opacity:1;display:block;visibility:visible;float:none}.main-navigation.toggled .main-nav li{float:none;clear:both;display:block;text-align:left}.main-navigation.toggled .main-nav li.hide-on-mobile{display:none!important}.main-navigation.toggled .menu-item-has-children .dropdown-menu-toggle{float:right}.main-navigation.toggled .menu li.search-item{display:none!important}.main-navigation.toggled .sf-menu>li.menu-item-float-right{float:none;display:inline-block}@media (max-width:768px){a,body,button,input{transition:all 0s ease-in-out}.top-bar .widget_nav_menu li{float:none;display:inline-block;padding:5px 0}.footer-bar .widget_nav_menu li:first-child{margin-left:10px}.footer-bar .widget_nav_menu li:last-child{margin-right:10px}.inside-header>:not(:last-child):not(.main-navigation){margin-bottom:20px}.site-header{text-align:center}.content-area,.sidebar{float:none;width:100%;left:0;right:0}.site-main{margin-left:0!important;margin-right:0!important}body:not(.no-sidebar) .site-main{margin-bottom:0!important}.separate-containers #left-sidebar+#right-sidebar .inside-right-sidebar{margin-top:0}.footer-bar .widget_nav_menu li{float:none;display:inline-block;padding:5px 0}}@font-face{font-display:swap;font-family:GeneratePress;src:url(https://randomnerdtutorials.com/wp-content/themes/generatepress/assets/fonts/generatepress.eot);font-weight:400;font-style:normal}.dropdown-menu-toggle:before,.menu-toggle:before,.nav-next .next:before,.nav-previous .prev:before,.search-item a:before{-moz-osx-font-smoothing:grayscale;-webkit-font-smoothing:antialiased;font-style:normal;font-variant:normal;text-rendering:auto;line-height:1}.nav-next .next:before,.nav-previous .prev:before{opacity:.7}.menu-toggle:before{content:"\f0c9";font-family:GeneratePress;width:1.28571429em;text-align:center;display:inline-block}.main-navigation.toggled .sfHover>a .dropdown-menu-toggle:before{content:"\f106"}.search-item a:before{content:"\f002";font-family:GeneratePress;width:1.28571429em;text-align:center;display:inline-block}.dropdown-menu-toggle:before{content:"\f107";font-family:GeneratePress;display:inline-block;width:.8em;text-align:left}nav:not(.toggled) ul ul .dropdown-menu-toggle:before{text-align:right}.dropdown-hover nav:not(.toggled) ul ul .dropdown-menu-toggle:before{content:"\f105"}.nav-next .next:before,.nav-previous .prev:before{font-family:GeneratePress;text-decoration:inherit;position:relative;margin-right:.6em;width:13px;text-align:center;display:inline-block}.nav-previous .prev:before{content:"\f104"}.nav-next .next:before{content:"\f105"}.button.rntyellow{padding:18px 20px;background:#e9cf31!important;color:#000!important;border:#d1b510 2px solid!important;font-weight:700;font-family:Arial,sans-serif;font-size:1.15em}.button.rntyellow:hover{background:#ffe338!important;border:#d1b510 2px solid!important;text-decoration:none!important}.button.rntyellow.rntsm{padding:6px;font-weight:400}.nav-links .page-numbers{background-color:#2f4468;padding:8px;color:#fff}.nav-links .page-numbers:hover{background-color:#0c2c68;color:#fff}.entry-content h2{position:relative}.entry-content h2::before{content:'';width:100%;height:3px;position:absolute;top:100%;left:0;background-color:#f5f5f5}.entry-content h2::after{content:'';width:10%;height:3px;position:absolute;top:100%;left:0;background-color:#2f4468}.category-product h1{text-align:center;font-size:36px}.no-sidebar.single .inside-article>*,.no-sidebar.page .inside-article>*{max-width:700px;margin-left:auto;margin-right:auto}.no-sidebar.single-post #primary-menu,.no-sidebar.single-post #site-navigation>div>button,.no-sidebar.single-post #site-navigation>div>div.mobile-bar-items,.no-sidebar.single-post #sticky-navigation>div>button,.no-sidebar.single-post #sticky-navigation>div>div.mobile-bar-items{display:none}.entry-content ul{list-style:square}@media (max-width:450px){ul{margin:0 0 1.5em 1.5em}}@media (min-width:768px){.entry-content>h2{margin-top:34px}}.entry-content{margin:1.1em 0 0}.rnt-sb-m a{text-decoration:none;color:#3a3a3a}.rnt-sb-m a:hover{text-decoration:underline;color:#3a3a3a}.rnt-sb-m .rnt-shl{position:relative;font-weight:700}.rnt-sb-m .rnt-shl::after{content:"";height:3px;background:#2f4468;position:absolute;left:0;width:50%;bottom:-2px}.rnt-sb-m p{margin-top:0;margin-bottom:14px}@media (max-width:1276px){#left-sidebar{display:none}.content-area{width:60%;left:0}}@media (max-width:1024px){.content-area{width:100%;float:none}}@media (max-width:1276px){#right-sidebar{width:334px!important}}@media (max-width:1000px){.rnt-menu-top-links{display:none}}@font-face{font-display:swap;font-family:eicons;src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.eot?5.11.0);src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.eot?5.11.0#iefix) format("embedded-opentype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.woff2?5.11.0) format("woff2"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.woff?5.11.0) format("woff"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.ttf?5.11.0) format("truetype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.svg?5.11.0#eicon) format("svg");font-weight:400;font-style:normal}@keyframes a{to{transform:rotate(359deg)}}.eicon-navigation-horizontal:before{content:'\e83d'}.eicon-nav-menu:before{content:'\e83e'}.eicon-navigation-vertical:before{content:'\e83f'}.eicon-post-navigation:before{content:'\e8b4'}.eicon-navigator:before{content:'\e8f1'}@keyframes swing{to{transform:rotate3d(0,0,1,0deg)}}@keyframes bounceIn{to{opacity:1;transform:scale3d(1,1,1)}}@keyframes bounceInDown{to{transform:none}}@keyframes bounceInLeft{to{transform:none}}@keyframes bounceInRight{0%{opacity:0;transform:translate3d(3000px,0,0)}to{transform:none}}@keyframes bounceInUp{0%{opacity:0;transform:translate3d(0,3000px,0)}to{transform:translate3d(0,0,0)}}@keyframes fadeIn{0%{opacity:0}to{opacity:1}}@keyframes fadeInDown{0%{opacity:0;transform:translate3d(0,-100%,0)}to{opacity:1;transform:none}}@keyframes fadeInLeft{0%{opacity:0;transform:translate3d(-100%,0,0)}to{opacity:1;transform:none}}@keyframes fadeInRight{0%{opacity:0;transform:translate3d(100%,0,0)}to{opacity:1;transform:none}}@keyframes fadeInUp{0%{opacity:0;transform:translate3d(0,100%,0)}to{opacity:1;transform:none}}@keyframes lightSpeedIn{0%{transform:translate3d(100%,0,0) skewX(-30deg);opacity:0}to{transform:none;opacity:1}}@keyframes rotateIn{0%{transform-origin:center;transform:rotate3d(0,0,1,-200deg);opacity:0}to{transform-origin:center;transform:none;opacity:1}}@keyframes rotateInDownLeft{0%{transform-origin:left bottom;transform:rotate3d(0,0,1,-45deg);opacity:0}to{transform-origin:left bottom;transform:none;opacity:1}}@keyframes rotateInDownRight{0%{transform-origin:right bottom;transform:rotate3d(0,0,1,45deg);opacity:0}to{transform-origin:right bottom;transform:none;opacity:1}}@keyframes rotateInUpLeft{0%{transform-origin:left bottom;transform:rotate3d(0,0,1,45deg);opacity:0}to{transform-origin:left bottom;transform:none;opacity:1}}@keyframes rotateInUpRight{0%{transform-origin:right bottom;transform:rotate3d(0,0,1,-90deg);opacity:0}to{transform-origin:right bottom;transform:none;opacity:1}}@keyframes rollIn{0%{opacity:0;transform:translate3d(-100%,0,0) rotate3d(0,0,1,-120deg)}to{opacity:1;transform:none}}@keyframes zoomIn{0%{opacity:0;transform:scale3d(.3,.3,.3)}}@keyframes zoomInDown{0%{opacity:0;transform:scale3d(.1,.1,.1) translate3d(0,-1000px,0);animation-timing-function:cubic-bezier(.55,.055,.675,.19)}}@keyframes zoomInLeft{0%{opacity:0;transform:scale3d(.1,.1,.1) translate3d(-1000px,0,0);animation-timing-function:cubic-bezier(.55,.055,.675,.19)}}@keyframes zoomInRight{0%{opacity:0;transform:scale3d(.1,.1,.1) translate3d(1000px,0,0);animation-timing-function:cubic-bezier(.55,.055,.675,.19)}}@keyframes zoomInUp{0%{opacity:0;transform:scale3d(.1,.1,.1) translate3d(0,1000px,0);animation-timing-function:cubic-bezier(.55,.055,.675,.19)}}@keyframes slideInDown{0%{transform:translate3d(0,-100%,0);visibility:visible}to{transform:translate3d(0,0,0)}}@keyframes slideInLeft{0%{transform:translate3d(-100%,0,0);visibility:visible}to{transform:translate3d(0,0,0)}}@keyframes slideInRight{0%{transform:translate3d(100%,0,0);visibility:visible}to{transform:translate3d(0,0,0)}}@keyframes slideInUp{0%{transform:translate3d(0,100%,0);visibility:visible}to{transform:translate3d(0,0,0)}}@keyframes elementor-animation-pulse-grow{to{transform:scale(1.1)}}@keyframes elementor-animation-pulse-shrink{to{transform:scale(.9)}}.elementor-column-gap-default>.elementor-row>.elementor-column>.elementor-element-populated{padding:10px}@media (max-width:767px){.elementor-reverse-mobile>.elementor-container>.elementor-row>:first-child{-webkit-box-ordinal-group:11;-ms-flex-order:10;order:10}.elementor-reverse-mobile>.elementor-container>.elementor-row>:nth-child(2){-webkit-box-ordinal-group:10;-ms-flex-order:9;order:9}.elementor-reverse-mobile>.elementor-container>.elementor-row>:nth-child(3){-webkit-box-ordinal-group:9;-ms-flex-order:8;order:8}.elementor-reverse-mobile>.elementor-container>.elementor-row>:nth-child(4){-webkit-box-ordinal-group:8;-ms-flex-order:7;order:7}.elementor-reverse-mobile>.elementor-container>.elementor-row>:nth-child(5){-webkit-box-ordinal-group:7;-ms-flex-order:6;order:6}.elementor-reverse-mobile>.elementor-container>.elementor-row>:nth-child(6){-webkit-box-ordinal-group:6;-ms-flex-order:5;order:5}.elementor-reverse-mobile>.elementor-container>.elementor-row>:nth-child(7){-webkit-box-ordinal-group:5;-ms-flex-order:4;order:4}.elementor-reverse-mobile>.elementor-container>.elementor-row>:nth-child(8){-webkit-box-ordinal-group:4;-ms-flex-order:3;order:3}.elementor-reverse-mobile>.elementor-container>.elementor-row>:nth-child(9){-webkit-box-ordinal-group:3;-ms-flex-order:2;order:2}.elementor-reverse-mobile>.elementor-container>.elementor-row>:nth-child(10){-webkit-box-ordinal-group:2;-ms-flex-order:1;order:1}.elementor-column{width:100%}}.elementor-screen-only,.screen-reader-text{position:absolute;top:-10000em;width:1px;height:1px;margin:-1px;padding:0;overflow:hidden;clip:rect(0,0,0,0);border:0}.elementor-clearfix:after{content:"";display:block;clear:both;width:0;height:0}.elementor{-webkit-hyphens:manual;-ms-hyphens:manual;hyphens:manual}.elementor *,.elementor :after,.elementor :before{-webkit-box-sizing:border-box;box-sizing:border-box}:root{--page-title-display:block}h1.entry-title{display:var(--page-title-display)}.elementor-section{position:relative}.elementor-section .elementor-container{display:-webkit-box;display:-ms-flexbox;display:flex;margin-right:auto;margin-left:auto;position:relative}@media (max-width:1024px){.elementor-section .elementor-container{-ms-flex-wrap:wrap;flex-wrap:wrap}}.elementor-section.elementor-section-boxed>.elementor-container{max-width:1140px}.elementor-row{width:100%;display:-webkit-box;display:-ms-flexbox;display:flex}@media (max-width:1024px){.elementor-row{-ms-flex-wrap:wrap;flex-wrap:wrap}}.elementor-widget-wrap{position:relative;width:100%;-ms-flex-wrap:wrap;flex-wrap:wrap;-ms-flex-line-pack:start;align-content:flex-start}.elementor:not(.elementor-bc-flex-widget) .elementor-widget-wrap{display:-webkit-box;display:-ms-flexbox;display:flex}.elementor-widget-wrap>.elementor-element{width:100%}.elementor-widget{position:relative}.elementor-widget:not(:last-child){margin-bottom:20px}.elementor-widget:not(:last-child).elementor-absolute,.elementor-widget:not(:last-child).elementor-widget__width-auto,.elementor-widget:not(:last-child).elementor-widget__width-initial{margin-bottom:0}.elementor-column{min-height:1px}.elementor-column,.elementor-column-wrap{position:relative;display:-webkit-box;display:-ms-flexbox;display:flex}.elementor-column-wrap{width:100%}@media (min-width:768px){.elementor-column.elementor-col-100{width:100%}}@media (max-width:767px){.elementor-reverse-mobile>.elementor-container>:first-child{-webkit-box-ordinal-group:11;-ms-flex-order:10;order:10}.elementor-reverse-mobile>.elementor-container>:nth-child(2){-webkit-box-ordinal-group:10;-ms-flex-order:9;order:9}.elementor-reverse-mobile>.elementor-container>:nth-child(3){-webkit-box-ordinal-group:9;-ms-flex-order:8;order:8}.elementor-reverse-mobile>.elementor-container>:nth-child(4){-webkit-box-ordinal-group:8;-ms-flex-order:7;order:7}.elementor-reverse-mobile>.elementor-container>:nth-child(5){-webkit-box-ordinal-group:7;-ms-flex-order:6;order:6}.elementor-reverse-mobile>.elementor-container>:nth-child(6){-webkit-box-ordinal-group:6;-ms-flex-order:5;order:5}.elementor-reverse-mobile>.elementor-container>:nth-child(7){-webkit-box-ordinal-group:5;-ms-flex-order:4;order:4}.elementor-reverse-mobile>.elementor-container>:nth-child(8){-webkit-box-ordinal-group:4;-ms-flex-order:3;order:3}.elementor-reverse-mobile>.elementor-container>:nth-child(9){-webkit-box-ordinal-group:3;-ms-flex-order:2;order:2}.elementor-reverse-mobile>.elementor-container>:nth-child(10){-webkit-box-ordinal-group:2;-ms-flex-order:1;order:1}.elementor-column{width:100%}}@-webkit-keyframes eicon-spin{to{-webkit-transform:rotate(359deg);transform:rotate(359deg)}}@keyframes eicon-spin{to{-webkit-transform:rotate(359deg);transform:rotate(359deg)}}.elementor-form-fields-wrapper{display:-webkit-box;display:-ms-flexbox;display:flex;-ms-flex-wrap:wrap;flex-wrap:wrap}.elementor-field-group{-ms-flex-wrap:wrap;flex-wrap:wrap;-webkit-box-align:center;-ms-flex-align:center;align-items:center}.elementor-field-group.elementor-field-type-submit{-webkit-box-align:end;-ms-flex-align:end;align-items:flex-end}.elementor-field-group .elementor-field-textual{width:100%;max-width:100%;border:1px solid #818a91;background-color:transparent;color:#373a3c;vertical-align:middle;-webkit-box-flex:1;-ms-flex-positive:1;flex-grow:1}.elementor-field-group .elementor-field-textual:focus{-webkit-box-shadow:0 0 0 1px rgba(0,0,0,.1) inset;box-shadow:inset 0 0 0 1px rgba(0,0,0,.1);outline:0}.elementor-field-group .elementor-field-textual::-webkit-input-placeholder{color:inherit;font-family:inherit;opacity:.6}.elementor-field-group .elementor-field-textual:-ms-input-placeholder{color:inherit;font-family:inherit;opacity:.6}.elementor-field-group .elementor-field-textual:-moz-placeholder,.elementor-field-group .elementor-field-textual::-moz-placeholder{color:inherit;font-family:inherit;opacity:.6}.elementor-field-group .elementor-field-textual::-ms-input-placeholder{color:inherit;font-family:inherit;opacity:.6}.elementor-field-group .elementor-field-textual::placeholder{color:inherit;font-family:inherit;opacity:.6}.elementor-field-label{cursor:pointer}.elementor-field-textual{line-height:1.4;font-size:15px;min-height:40px;padding:5px 14px;-webkit-border-radius:3px;border-radius:3px}.elementor-button-align-stretch .elementor-field-type-submit:not(.e-form__buttons__wrapper) .elementor-button{-ms-flex-preferred-size:100%;flex-basis:100%}.elementor-form .elementor-button{padding-top:0;padding-bottom:0;border:0}.elementor-form .elementor-button>span{display:-webkit-box;display:-ms-flexbox;display:flex;-webkit-box-pack:center;-ms-flex-pack:center;justify-content:center}.elementor-form .elementor-button.elementor-size-md{min-height:47px}.elementor-element .elementor-widget-container{-webkit-transition:background .3s,border .3s,-webkit-border-radius .3s,-webkit-box-shadow .3s;transition:background .3s,border .3s,-webkit-border-radius .3s,-webkit-box-shadow .3s;-o-transition:background .3s,border .3s,border-radius .3s,box-shadow .3s;transition:background .3s,border .3s,border-radius .3s,box-shadow .3s;transition:background .3s,border .3s,border-radius .3s,box-shadow .3s,-webkit-border-radius .3s,-webkit-box-shadow .3s}.elementor-button{display:inline-block;line-height:1;background-color:#818a91;font-size:15px;padding:12px 24px;-webkit-border-radius:3px;border-radius:3px;color:#fff;fill:#fff;text-align:center;-webkit-transition:all .3s;-o-transition:all .3s;transition:all .3s}.elementor-button:focus,.elementor-button:hover,.elementor-button:visited{color:#fff}.elementor-button-icon{-webkit-box-flex:0;-ms-flex-positive:0;flex-grow:0;-webkit-box-ordinal-group:6;-ms-flex-order:5;order:5}.elementor-button-text{-webkit-box-flex:1;-ms-flex-positive:1;flex-grow:1;-webkit-box-ordinal-group:11;-ms-flex-order:10;order:10;display:inline-block}.elementor-button.elementor-size-md{font-size:16px;padding:15px 30px;-webkit-border-radius:4px;border-radius:4px}.elementor-button span{text-decoration:inherit}.elementor-heading-title{padding:0;margin:0;line-height:1}@-webkit-keyframes swiper-preloader-spin{to{-webkit-transform:rotate(1turn);transform:rotate(1turn)}}@keyframes swiper-preloader-spin{to{-webkit-transform:rotate(1turn);transform:rotate(1turn)}}@media (max-width:767px){.elementor .elementor-hidden-phone{display:none}}.elementor-kit-94299{--e-global-color-primary:#6EC1E4;--e-global-color-secondary:#54595F;--e-global-color-text:#7A7A7A;--e-global-color-accent:#61CE70;--e-global-color-169bfe26:#4054B2;--e-global-color-6f35190b:#23A455;--e-global-color-71ce0ad5:#000;--e-global-color-32c765ac:#FFF;--e-global-typography-primary-font-family:"Roboto";--e-global-typography-primary-font-weight:600;--e-global-typography-secondary-font-family:"Roboto Slab";--e-global-typography-secondary-font-weight:400;--e-global-typography-text-font-family:"Roboto";--e-global-typography-text-font-weight:400;--e-global-typography-accent-font-family:"Roboto";--e-global-typography-accent-font-weight:500}.elementor-section.elementor-section-boxed>.elementor-container{max-width:1380px}.elementor-widget:not(:last-child){margin-bottom:20px}h1.entry-title{display:var(--page-title-display)}@media (max-width:1024px){.elementor-section.elementor-section-boxed>.elementor-container{max-width:1024px}}@media (max-width:767px){.elementor-section.elementor-section-boxed>.elementor-container{max-width:767px}}.e-form__buttons{-ms-flex-wrap:wrap;flex-wrap:wrap}.e-form__buttons{display:-webkit-box;display:-ms-flexbox;display:flex}.elementor-form .elementor-button>span{display:-webkit-box;display:-ms-flexbox;display:flex;-webkit-box-pack:center;-ms-flex-pack:center;justify-content:center;-webkit-box-align:center;-ms-flex-align:center;align-items:center}.elementor-form .elementor-button .elementor-button-text{white-space:normal;-webkit-box-flex:0;-ms-flex-positive:0;flex-grow:0}.elementor-products-grid nav.woocommerce-pagination{margin-top:40px}.elementor-products-grid:not(.elementor-show-pagination-border-yes) nav.woocommerce-pagination ul{border:0}.elementor-products-grid:not(.elementor-show-pagination-border-yes) nav.woocommerce-pagination ul li{border-right:0;border-left:0}@-webkit-keyframes elementor-headline-dash{to{stroke-dasharray:1500 1500;opacity:1}}@keyframes elementor-headline-dash{to{stroke-dasharray:1500 1500;opacity:1}}@-webkit-keyframes hide-highlight{to{opacity:0;-webkit-filter:blur(10px);filter:blur(10px)}}@keyframes hide-highlight{to{opacity:0;-webkit-filter:blur(10px);filter:blur(10px)}}@-webkit-keyframes elementor-headline-flip-in{to{-webkit-transform:rotateX(1turn);transform:rotateX(1turn);opacity:1}}@keyframes elementor-headline-flip-in{to{-webkit-transform:rotateX(1turn);transform:rotateX(1turn);opacity:1}}@-webkit-keyframes elementor-headline-flip-out{to{-webkit-transform:rotateX(180deg);transform:rotateX(180deg);opacity:0}}@keyframes elementor-headline-flip-out{to{-webkit-transform:rotateX(180deg);transform:rotateX(180deg);opacity:0}}@-webkit-keyframes elementor-headline-pulse{to{-webkit-transform:translateY(-50%) scale(0);transform:translateY(-50%) scale(0);opacity:0}}@keyframes elementor-headline-pulse{to{-webkit-transform:translateY(-50%) scale(0);transform:translateY(-50%) scale(0);opacity:0}}@-webkit-keyframes elementor-headline-swirl-in{to{opacity:1;-webkit-transform:translateZ(-20px) rotateX(0deg);transform:translateZ(-20px) rotateX(0deg)}}@keyframes elementor-headline-swirl-in{to{opacity:1;-webkit-transform:translateZ(-20px) rotateX(0deg);transform:translateZ(-20px) rotateX(0deg)}}@-webkit-keyframes elementor-headline-swirl-out{to{opacity:0;-webkit-transform:translateZ(-20px) rotateX(-90deg);transform:translateZ(-20px) rotateX(-90deg)}}@keyframes elementor-headline-swirl-out{to{opacity:0;-webkit-transform:translateZ(-20px) rotateX(-90deg);transform:translateZ(-20px) rotateX(-90deg)}}@-webkit-keyframes elementor-headline-slide-down-in{to{opacity:1;-webkit-transform:translateY(0);transform:translateY(0)}}@keyframes elementor-headline-slide-down-in{to{opacity:1;-webkit-transform:translateY(0);transform:translateY(0)}}@-webkit-keyframes elementor-headline-slide-down-out{to{opacity:0;-webkit-transform:translateY(100%);transform:translateY(100%)}}@keyframes elementor-headline-slide-down-out{to{opacity:0;-webkit-transform:translateY(100%);transform:translateY(100%)}}@-webkit-keyframes elementor-headline-drop-in-in{to{opacity:1;-webkit-transform:translateZ(0);transform:translateZ(0)}}@keyframes elementor-headline-drop-in-in{to{opacity:1;-webkit-transform:translateZ(0);transform:translateZ(0)}}@-webkit-keyframes elementor-headline-drop-in-out{to{opacity:0;-webkit-transform:translateZ(-100px);transform:translateZ(-100px)}}@keyframes elementor-headline-drop-in-out{to{opacity:0;-webkit-transform:translateZ(-100px);transform:translateZ(-100px)}}@-webkit-keyframes elementor-headline-blinds-in{to{-webkit-transform:rotateY(0deg);transform:rotateY(0deg)}}@keyframes elementor-headline-blinds-in{to{-webkit-transform:rotateY(0deg);transform:rotateY(0deg)}}@-webkit-keyframes elementor-headline-blinds-out{to{-webkit-transform:rotateY(-180deg);transform:rotateY(-180deg)}}@keyframes elementor-headline-blinds-out{to{-webkit-transform:rotateY(-180deg);transform:rotateY(-180deg)}}@-webkit-keyframes elementor-headline-wave-up{to{-webkit-transform:scale(1);transform:scale(1);opacity:1}}@keyframes elementor-headline-wave-up{to{-webkit-transform:scale(1);transform:scale(1);opacity:1}}@-webkit-keyframes elementor-headline-slide-in{to{opacity:1;-webkit-transform:translateX(0);transform:translateX(0)}}@keyframes elementor-headline-slide-in{to{opacity:1;-webkit-transform:translateX(0);transform:translateX(0)}}@-webkit-keyframes elementor-headline-slide-out{to{opacity:0;-webkit-transform:translateX(100%);transform:translateX(100%)}}@keyframes elementor-headline-slide-out{to{opacity:0;-webkit-transform:translateX(100%);transform:translateX(100%)}}.site-main .menu-navigation-container{overflow:visible}.elementor-nav-menu--main .elementor-nav-menu a{-webkit-transition:.4s;-o-transition:.4s;transition:.4s}.elementor-nav-menu--main .elementor-nav-menu a,.elementor-nav-menu--main .elementor-nav-menu a.highlighted,.elementor-nav-menu--main .elementor-nav-menu a:focus,.elementor-nav-menu--main .elementor-nav-menu a:hover{padding:13px 20px}.elementor-nav-menu--main .elementor-nav-menu a.current{background:#373a3c;color:#fff}.elementor-nav-menu--main .elementor-nav-menu a.disabled{background:#55595c;color:#a1a6a9}.elementor-nav-menu--main .elementor-nav-menu ul{position:absolute;width:12em;border-width:0;border-style:solid;padding:0}.elementor-nav-menu--main .elementor-nav-menu span.scroll-down,.elementor-nav-menu--main .elementor-nav-menu span.scroll-up{position:absolute;display:none;visibility:hidden;overflow:hidden;background:#fff;height:20px}.elementor-nav-menu--main .elementor-nav-menu span.scroll-down-arrow,.elementor-nav-menu--main .elementor-nav-menu span.scroll-up-arrow{position:absolute;top:-2px;left:50%;margin-left:-8px;width:0;height:0;overflow:hidden;border:8px dashed transparent;border-bottom:8px solid #494c4f}.elementor-nav-menu--main .elementor-nav-menu span.scroll-down-arrow{top:6px;border-style:solid dashed dashed;border-color:#494c4f transparent transparent}.elementor-nav-menu--main .elementor-nav-menu--dropdown .sub-arrow i{-webkit-transform:rotate(-90deg);-ms-transform:rotate(-90deg);transform:rotate(-90deg)}.elementor-nav-menu--layout-horizontal{display:-webkit-box;display:-ms-flexbox;display:flex}.elementor-nav-menu--layout-horizontal .elementor-nav-menu{display:-webkit-box;display:-ms-flexbox;display:flex;-ms-flex-wrap:wrap;flex-wrap:wrap}.elementor-nav-menu--layout-horizontal .elementor-nav-menu a{white-space:nowrap}.elementor-nav-menu__align-right .elementor-nav-menu{margin-left:auto;-webkit-box-pack:end;-ms-flex-pack:end;justify-content:flex-end}.elementor-nav-menu__align-right .elementor-nav-menu--layout-vertical>ul>li>a{-webkit-box-pack:end;-ms-flex-pack:end;justify-content:flex-end}.elementor-nav-menu__align-left .elementor-nav-menu{margin-right:auto;-webkit-box-pack:start;-ms-flex-pack:start;justify-content:flex-start}.elementor-nav-menu__align-left .elementor-nav-menu--layout-vertical>ul>li>a{-webkit-box-pack:start;-ms-flex-pack:start;justify-content:flex-start}.elementor-nav-menu__align-center .elementor-nav-menu{margin-left:auto;margin-right:auto;-webkit-box-pack:center;-ms-flex-pack:center;justify-content:center}.elementor-nav-menu__align-center .elementor-nav-menu--layout-vertical>ul>li>a{-webkit-box-pack:center;-ms-flex-pack:center;justify-content:center}.elementor-nav-menu__align-justify .elementor-nav-menu--layout-horizontal .elementor-nav-menu{width:100%}.elementor-nav-menu__align-justify .elementor-nav-menu--layout-horizontal .elementor-nav-menu>li{-webkit-box-flex:1;-ms-flex-positive:1;flex-grow:1}.elementor-nav-menu__align-justify .elementor-nav-menu--layout-horizontal .elementor-nav-menu>li>a{-webkit-box-pack:center;-ms-flex-pack:center;justify-content:center}.elementor-widget-nav-menu:not(.elementor-nav-menu--toggle) .elementor-menu-toggle{display:none}.elementor-widget-nav-menu .elementor-widget-container{display:-webkit-box;display:-ms-flexbox;display:flex;-webkit-box-orient:vertical;-webkit-box-direction:normal;-ms-flex-direction:column;flex-direction:column}.elementor-nav-menu{position:relative;z-index:2}.elementor-nav-menu:after{content:"\00a0";display:block;height:0;font:0/0 serif;clear:both;visibility:hidden;overflow:hidden}.elementor-nav-menu,.elementor-nav-menu li,.elementor-nav-menu ul{display:block;list-style:none;margin:0;padding:0;line-height:normal;-webkit-tap-highlight-color:transparent}.elementor-nav-menu ul{display:none}.elementor-nav-menu ul ul a,.elementor-nav-menu ul ul a:active,.elementor-nav-menu ul ul a:focus,.elementor-nav-menu ul ul a:hover{border-left:16px solid transparent}.elementor-nav-menu ul ul ul a,.elementor-nav-menu ul ul ul a:active,.elementor-nav-menu ul ul ul a:focus,.elementor-nav-menu ul ul ul a:hover{border-left:24px solid transparent}.elementor-nav-menu ul ul ul ul a,.elementor-nav-menu ul ul ul ul a:active,.elementor-nav-menu ul ul ul ul a:focus,.elementor-nav-menu ul ul ul ul a:hover{border-left:32px solid transparent}.elementor-nav-menu ul ul ul ul ul a,.elementor-nav-menu ul ul ul ul ul a:active,.elementor-nav-menu ul ul ul ul ul a:focus,.elementor-nav-menu ul ul ul ul ul a:hover{border-left:40px solid transparent}.elementor-nav-menu a,.elementor-nav-menu li{position:relative}.elementor-nav-menu li{border-width:0}.elementor-nav-menu a{display:-webkit-box;display:-ms-flexbox;display:flex;-webkit-box-align:center;-ms-flex-align:center;align-items:center}.elementor-nav-menu a,.elementor-nav-menu a:focus,.elementor-nav-menu a:hover{padding:10px 20px;line-height:20px}.elementor-nav-menu a.current{background:#373a3c;color:#fff}.elementor-nav-menu a.disabled{cursor:not-allowed;color:#a1a6a9}.elementor-nav-menu--indicator-none .elementor-nav-menu .elementor-item.has-submenu{padding-right:20px}.elementor-nav-menu--indicator-none .elementor-nav-menu .elementor-item.has-submenu .sub-arrow{display:none}.elementor-nav-menu--indicator-plus:before{font-family:Open Sans,sans-serif}.elementor-nav-menu--indicator-chevron .elementor-nav-menu .sub-arrow{font-size:10px}.elementor-nav-menu--indicator-chevron .elementor-nav-menu .sub-arrow i:before{content:""}.elementor-nav-menu--indicator-angle .elementor-nav-menu .sub-arrow i:before{content:""}.elementor-nav-menu--indicator-classic .elementor-nav-menu .sub-arrow i:before{content:""}.elementor-nav-menu--indicator-plus .elementor-nav-menu .sub-arrow i:before{content:"+"}.elementor-nav-menu .sub-arrow{font-size:16px;line-height:1;padding:10px 0 10px 10px;margin-top:-10px;margin-bottom:-10px}.elementor-nav-menu .sub-arrow i{pointer-events:none}.elementor-nav-menu--dropdown .elementor-item.elementor-item-active,.elementor-nav-menu--dropdown .elementor-item.highlighted,.elementor-nav-menu--dropdown .elementor-item:focus,.elementor-nav-menu--dropdown .elementor-item:hover{background-color:#55595c;color:#fff}.elementor-nav-menu--dropdown{background-color:#fff;font-size:13px}.elementor-nav-menu--dropdown-none .elementor-menu-toggle,.elementor-nav-menu--dropdown-none .elementor-nav-menu--dropdown{display:none}.elementor-nav-menu--dropdown.elementor-nav-menu__container{margin-top:10px;-webkit-transition:max-height .3s,-webkit-transform .3s;transition:max-height .3s,-webkit-transform .3s;-o-transition:max-height .3s,transform .3s;transition:max-height .3s,transform .3s;transition:max-height .3s,transform .3s,-webkit-transform .3s;-webkit-transform-origin:top;-ms-transform-origin:top;transform-origin:top;overflow:auto}.elementor-nav-menu--dropdown.elementor-nav-menu__container .elementor-sub-item{font-size:.85em}.elementor-nav-menu--dropdown a{color:#494c4f;-webkit-box-pack:justify;-ms-flex-pack:justify;justify-content:space-between}.elementor-nav-menu--dropdown a.current{background:#373a3c;color:#fff}.elementor-nav-menu--dropdown a.disabled{color:#b3b3b3}ul.elementor-nav-menu--dropdown a,ul.elementor-nav-menu--dropdown a:focus,ul.elementor-nav-menu--dropdown a:hover{text-shadow:none;border-left:8px solid transparent}.elementor-nav-menu__text-align-center .elementor-nav-menu--dropdown .elementor-nav-menu a{-webkit-box-pack:center;-ms-flex-pack:center;justify-content:center}.elementor-nav-menu--toggle .elementor-menu-toggle:not(.elementor-active)+.elementor-nav-menu__container{-webkit-transform:scaleY(0);-ms-transform:scaleY(0);transform:scaleY(0);max-height:0}.elementor-nav-menu--toggle .elementor-menu-toggle.elementor-active+.elementor-nav-menu__container{-webkit-transform:scaleY(1);-ms-transform:scaleY(1);transform:scaleY(1);max-height:100vh}.elementor-nav-menu--stretch .elementor-nav-menu__container.elementor-nav-menu--dropdown{position:absolute;z-index:9997}@media (min-width:768px){.elementor-nav-menu--dropdown-mobile .elementor-menu-toggle,.elementor-nav-menu--dropdown-mobile .elementor-nav-menu--dropdown{display:none}}@media (min-width:1025px){.elementor-nav-menu--dropdown-tablet .elementor-menu-toggle,.elementor-nav-menu--dropdown-tablet .elementor-nav-menu--dropdown{display:none}}@media (max-width:1024px){.elementor-nav-menu--dropdown-tablet .elementor-nav-menu--main{display:none}}@media (max-width:767px){.elementor-nav-menu--dropdown-mobile .elementor-nav-menu--main{display:none}}.elementor-post-navigation-borders-yes .elementor-post-navigation.elementor-grid{color:#d4d4d4;border:1px solid;border-right:none;border-left:none;padding-top:10px;padding-bottom:10px}.elementor-post-navigation-borders-yes .elementor-post-navigation__separator{height:100%;width:1px;margin:0 auto;background-color:#d4d4d4}.elementor-post-navigation{overflow:hidden;display:-webkit-box;display:-ms-flexbox;display:flex}.elementor-post-navigation .post-navigation__arrow-wrapper{color:#d4d4d4}.elementor-post-navigation .post-navigation__arrow-wrapper.post-navigation__arrow-prev{font-size:30px;padding-right:15px}.elementor-post-navigation .post-navigation__arrow-wrapper.post-navigation__arrow-next{font-size:30px;padding-left:15px}.elementor-post-navigation .post-navigation__arrow-wrapper i{-webkit-transform:translateY(-5%);-ms-transform:translateY(-5%);transform:translateY(-5%)}.elementor-post-navigation .elementor-post-navigation__link__next,.elementor-post-navigation .elementor-post-navigation__link__prev{overflow:hidden}.elementor-post-navigation .elementor-post-navigation__link a{display:-webkit-box;display:-ms-flexbox;display:flex;-webkit-box-align:center;-ms-flex-align:center;align-items:center;max-width:100%}.elementor-post-navigation .post-navigation__next--label,.elementor-post-navigation .post-navigation__prev--label{text-transform:uppercase;font-size:.8em}.elementor-post-navigation .post-navigation__next--title,.elementor-post-navigation .post-navigation__prev--title{font-size:.7em}.elementor-post-navigation .post-navigation__next--label,.elementor-post-navigation .post-navigation__next--title,.elementor-post-navigation .post-navigation__prev--label,.elementor-post-navigation .post-navigation__prev--title{overflow:hidden;-o-text-overflow:ellipsis;text-overflow:ellipsis}.elementor-post-navigation span.elementor-post-navigation__link__next{text-align:right}.elementor-post-navigation span.elementor-post-navigation__link__next,.elementor-post-navigation span.elementor-post-navigation__link__prev{display:-webkit-box;display:-ms-flexbox;display:flex;-webkit-box-orient:vertical;-webkit-box-direction:normal;-ms-flex-direction:column;flex-direction:column}.elementor-post-navigation .elementor-grid{-webkit-box-pack:justify;-ms-flex-pack:justify;justify-content:space-between}.elementor-post-navigation .elementor-post-navigation__link{width:calc(50% - (1px/2));white-space:nowrap;overflow:hidden;-o-text-overflow:ellipsis;text-overflow:ellipsis}.elementor-post-navigation .elementor-post-navigation__separator-wrapper{text-align:center}.elementor-post-navigation .elementor-post-navigation__next{text-align:right}.elementor-post-navigation .elementor-post-navigation__next a{float:right}[data-elementor-type=popup]:not(.elementor-edit-area){display:none}[data-elementor-type=popup] .elementor-section-wrap:not(:empty)+#elementor-add-new-section{display:none}@-webkit-keyframes fa-spin{to{-webkit-transform:rotate(1turn);transform:rotate(1turn)}}@keyframes fa-spin{to{-webkit-transform:rotate(1turn);transform:rotate(1turn)}}@font-face{font-display:swap;font-family:"Font Awesome 5 Brands";font-style:normal;font-weight:400;font-display:swap;src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-brands-400.eot);src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-brands-400.eot#iefix) format("embedded-opentype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-brands-400.woff2) format("woff2"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-brands-400.woff) format("woff"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-brands-400.ttf) format("truetype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-brands-400.svg#fontawesome) format("svg")}@font-face{font-display:swap;font-family:"Font Awesome 5 Free";font-style:normal;font-weight:400;font-display:swap;src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-regular-400.eot);src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-regular-400.eot#iefix) format("embedded-opentype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-regular-400.woff2) format("woff2"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-regular-400.woff) format("woff"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-regular-400.ttf) format("truetype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-regular-400.svg#fontawesome) format("svg")}@font-face{font-display:swap;font-family:"Font Awesome 5 Free";font-style:normal;font-weight:900;font-display:swap;src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-solid-900.eot);src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-solid-900.eot#iefix) format("embedded-opentype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-solid-900.woff2) format("woff2"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-solid-900.woff) format("woff"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-solid-900.ttf) format("truetype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/font-awesome/webfonts/fa-solid-900.svg#fontawesome) format("svg")}.fa.fa-navicon:before{content:"\f0c9"}.elementor-83058 .elementor-element.elementor-element-544e0740>.elementor-container>.elementor-row>.elementor-column>.elementor-column-wrap>.elementor-widget-wrap{align-content:flex-end;align-items:flex-end}.elementor-83058 .elementor-element.elementor-element-544e0740{transition:background .3s,border .3s,border-radius .3s,box-shadow .3s;padding:0 50% 0 4%}.elementor-83058 .elementor-element.elementor-element-676b082e>.elementor-column-wrap>.elementor-widget-wrap>.elementor-widget:not(.elementor-widget__width-auto):not(.elementor-widget__width-initial):not(:last-child):not(.elementor-absolute){margin-bottom:0}.elementor-83058 .elementor-element.elementor-element-5eee063c{text-align:left}.elementor-83058 .elementor-element.elementor-element-5eee063c .elementor-heading-title{font-size:44px;font-weight:700}.elementor-83058 .elementor-element.elementor-element-5eee063c>.elementor-widget-container{margin:0 0 15px 0;padding:0 0 0 0}.elementor-83058 .elementor-element.elementor-element-9bd904c{font-size:17px}.elementor-83058 .elementor-element.elementor-element-2a77907 .elementor-field-group{padding-right:calc(10px/2);padding-left:calc(10px/2);margin-bottom:10px}.elementor-83058 .elementor-element.elementor-element-2a77907 .elementor-form-fields-wrapper{margin-left:calc(-10px/2);margin-right:calc(-10px/2);margin-bottom:-10px}.elementor-83058 .elementor-element.elementor-element-2a77907 .elementor-field-group:not(.elementor-field-type-upload) .elementor-field:not(.elementor-select-wrapper){background-color:#fff}.elementor-83058 .elementor-element.elementor-element-2a77907 .elementor-button[type=submit]{background-color:#0268dd;color:#fff}.elementor-83058 .elementor-element.elementor-element-2a77907 .elementor-button[type=submit]:hover{background-color:#026cf7;color:#fff}.elementor-83058 .elementor-element.elementor-element-2a77907 .elementor-button{border-radius:0 0 0 0}.elementor-83058 .elementor-element.elementor-element-2a77907{--e-form-steps-indicators-spacing:20px;--e-form-steps-indicator-padding:30px;--e-form-steps-indicator-inactive-secondary-color:#ffffff;--e-form-steps-indicator-active-secondary-color:#ffffff;--e-form-steps-indicator-completed-secondary-color:#ffffff;--e-form-steps-divider-width:1px;--e-form-steps-divider-gap:10px}.elementor-83058 .elementor-element.elementor-element-2a77907>.elementor-widget-container{margin:0 0 0 0;padding:0 0 0 0}@media (max-width:1024px){.elementor-83058 .elementor-element.elementor-element-5eee063c .elementor-heading-title{font-size:38px}}@media (max-width:767px){.elementor-83058 .elementor-element.elementor-element-544e0740{margin-top:-140px;margin-bottom:0;padding:10px 10px 10px 10px}.elementor-83058 .elementor-element.elementor-element-5eee063c{text-align:center}.elementor-83058 .elementor-element.elementor-element-5eee063c .elementor-heading-title{font-size:28px}.elementor-83058 .elementor-element.elementor-element-2a77907>.elementor-widget-container{margin:0 0 0 0;padding:0 0 0 0}}.sticky-enabled .gen-sidebar-nav.is_stuck .main-navigation{margin-bottom:0}.sticky-enabled .gen-sidebar-nav.is_stuck{z-index:500}.sticky-enabled .main-navigation.is_stuck{box-shadow:0 2px 2px -2px rgba(0,0,0,.2)}.navigation-stick:not(.gen-sidebar-nav){left:0;right:0;width:100%!important}.both-sticky-menu .main-navigation:not(#mobile-header).toggled .main-nav,.mobile-sticky-menu .main-navigation:not(#mobile-header).toggled .main-nav{clear:both}.both-sticky-menu .main-navigation:not(#mobile-header).toggled .main-nav>ul,.mobile-header-sticky #mobile-header.toggled .main-nav>ul,.mobile-sticky-menu .main-navigation:not(#mobile-header).toggled .main-nav>ul{position:absolute;left:0;right:0;z-index:999}#sticky-placeholder .navigation-branding,#sticky-placeholder.mobile-header-navigation .mobile-header-logo{display:none}.nav-float-right .is_stuck.main-navigation:not(.toggled) .menu>li{float:none;display:inline-block}.nav-float-right .is_stuck.main-navigation:not(.toggled) .menu>li.search-item,.nav-float-right .is_stuck.main-navigation:not(.toggled) .menu>li.slideout-toggle,.nav-float-right .is_stuck.main-navigation:not(.toggled) .menu>li.wc-menu-item{display:block;float:right}.nav-float-right .is_stuck.main-navigation:not(.toggled) ul{letter-spacing:-.31em;font-size:1em}.nav-float-right .is_stuck.main-navigation:not(.toggled) ul li{letter-spacing:normal}.nav-float-right .is_stuck.main-navigation:not(.toggled){text-align:right}.nav-float-right .is_stuck.main-navigation.has-branding:not(.toggled) ul,.nav-float-right .is_stuck.main-navigation.has-sticky-branding:not(.toggled) ul{letter-spacing:unset}.nav-float-right .is_stuck.main-navigation.has-branding:not(.toggled) .menu>li,.nav-float-right .is_stuck.main-navigation.has-sticky-branding:not(.toggled) .menu>li{display:block;float:left}.main-navigation .navigation-logo{float:left;display:block;margin-left:-10px;transition:height .3s ease;opacity:1}.main-navigation .navigation-logo img{position:relative;vertical-align:middle;padding:10px;display:block;box-sizing:border-box;transition:height .3s ease}.nav-float-left .main-navigation .navigation-logo{float:right}.nav-float-left .main-navigation .navigation-logo{margin-left:0;margin-right:-10px}.regular-menu-logo .navigation-stick .navigation-logo,.sticky-menu-logo .main-navigation .navigation-logo{display:none!important}.sticky-menu-logo .navigation-stick:not(#sticky-placeholder) .navigation-logo{display:block!important}.main-navigation .inside-navigation:not(.grid-container) .navigation-logo,.main-navigation.grid-container .navigation-logo{margin-left:0}.gen-sidebar-nav .main-navigation .navigation-logo{float:none;padding:0;margin:30px 0!important;text-align:center}.gen-sidebar-nav .main-navigation .navigation-logo img{height:auto;max-width:100%;vertical-align:bottom;padding:0;margin:0 auto}body[class*=nav-float-].menu-logo-enabled:not(.sticky-menu-logo) .main-navigation .main-nav,body[class*=nav-float-].menu-logo-enabled:not(.sticky-menu-logo) .main-navigation .navigation-logo{display:inline-block;vertical-align:middle}body[class*=nav-float-].menu-logo-enabled:not(.sticky-menu-logo) .main-navigation:not(.navigation-stick) .navigation-logo{margin:0}.using-floats .main-navigation:not(.slideout-navigation) .inside-navigation:after,.using-floats .main-navigation:not(.slideout-navigation) .inside-navigation:before{content:".";display:block;overflow:hidden;visibility:hidden;font-size:0;line-height:0;width:0;height:0}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOiCnqEu92Fr1Mu51QrEz0dL-vwnYh2eg.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOiCnqEu92Fr1Mu51QrEzQdL-vwnYh2eg.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOiCnqEu92Fr1Mu51QrEzwdL-vwnYh2eg.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOiCnqEu92Fr1Mu51QrEzMdL-vwnYh2eg.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOiCnqEu92Fr1Mu51QrEz8dL-vwnYh2eg.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOiCnqEu92Fr1Mu51QrEz4dL-vwnYh2eg.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOiCnqEu92Fr1Mu51QrEzAdL-vwnYg.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TjASc3CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TjASc-CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TjASc2CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TjASc5CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TjASc1CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TjASc0CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TjASc6CsTYl4BO.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1Mu51xFIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1Mu51xMIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1Mu51xEIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1Mu51xLIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1Mu51xHIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1Mu51xGIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1Mu51xIIzIXKMny.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51S7ACc3CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51S7ACc-CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51S7ACc2CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51S7ACc5CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51S7ACc1CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51S7ACc0CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51S7ACc6CsTYl4BO.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TzBic3CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TzBic-CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TzBic2CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TzBic5CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TzBic1CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TzBic0CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TzBic6CsTYl4BO.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TLBCc3CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TLBCc-CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TLBCc2CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TLBCc5CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TLBCc1CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TLBCc0CsTYl4BOQ3o.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:italic;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOjCnqEu92Fr1Mu51TLBCc6CsTYl4BO.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1MmgVxFIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1MmgVxMIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1MmgVxEIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1MmgVxLIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1MmgVxHIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1MmgVxGIzIXKMnyrYk.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOkCnqEu92Fr1MmgVxIIzIXKMny.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmSU5fCRc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmSU5fABc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmSU5fCBc4AMP6lbBP.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmSU5fBxc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmSU5fCxc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmSU5fChc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmSU5fBBc4AMP6lQ.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOmCnqEu92Fr1Mu72xKKTU1Kvnz.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOmCnqEu92Fr1Mu5mxKKTU1Kvnz.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOmCnqEu92Fr1Mu7mxKKTU1Kvnz.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOmCnqEu92Fr1Mu4WxKKTU1Kvnz.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOmCnqEu92Fr1Mu7WxKKTU1Kvnz.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOmCnqEu92Fr1Mu7GxKKTU1Kvnz.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOmCnqEu92Fr1Mu4mxKKTU1Kg.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmEU9fCRc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmEU9fABc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmEU9fCBc4AMP6lbBP.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmEU9fBxc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmEU9fCxc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmEU9fChc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmEU9fBBc4AMP6lQ.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmWUlfCRc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmWUlfABc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmWUlfCBc4AMP6lbBP.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmWUlfBxc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmWUlfCxc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmWUlfChc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmWUlfBBc4AMP6lQ.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmYUtfCRc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmYUtfABc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmYUtfCBc4AMP6lbBP.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmYUtfBxc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmYUtfCxc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmYUtfChc4AMP6lbBP.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/KFOlCnqEu92Fr1MmYUtfBBc4AMP6lQ.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufA5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufJ5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufB5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufO5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufC5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufD5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:100;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufN5qWr4xCC.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:200;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufA5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:200;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufJ5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:200;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufB5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:200;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufO5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:200;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufC5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:200;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufD5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:200;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufN5qWr4xCC.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufA5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufJ5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufB5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufO5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufC5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufD5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:300;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufN5qWr4xCC.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufA5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufJ5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufB5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufO5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufC5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufD5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:400;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufN5qWr4xCC.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufA5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufJ5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufB5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufO5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufC5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufD5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:500;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufN5qWr4xCC.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:600;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufA5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:600;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufJ5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:600;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufB5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:600;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufO5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:600;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufC5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:600;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufD5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:600;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufN5qWr4xCC.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufA5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufJ5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufB5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufO5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufC5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufD5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:700;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufN5qWr4xCC.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:800;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufA5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:800;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufJ5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:800;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufB5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:800;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufO5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:800;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufC5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:800;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufD5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:800;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufN5qWr4xCC.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufA5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufJ5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufB5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufO5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufC5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+1EA0-1EF9,U+20AB}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufD5qWr4xCCQ_k.woff2) format('woff2');unicode-range:U+0100-024F,U+0259,U+1E00-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-display:swap;font-family:'Roboto Slab';font-style:normal;font-weight:900;src:url(https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/BngMUXZYTXPIvIBgJJSb6ufN5qWr4xCC.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}.presentation-wrapper-fullscreen .nav-arrow-left,.presentation-wrapper-fullscreen .nav-arrow-right{z-index:20001}.presentation-wrapper-fullscreen .nav-fullscreen-button{z-index:20002}.presentation .nav-arrow-left,.presentation .nav-arrow-right,.presentation .nav-fullscreen-button{position:absolute;width:34px;background-repeat:no-repeat;z-index:2;opacity:0;transition:opacity .25s}.presentation .nav-arrow-left,.presentation .nav-arrow-right{height:100%;background-image:url(https://randomnerdtutorials.com/wp-content/plugins/jetpack/modules/shortcodes/images/slide-nav.png);background-size:450% 61px}.presentation .nav-arrow-left{left:0;background-position:4px 50%}.presentation .nav-arrow-right{right:0;background-position:-120px 50%}.presentation .nav-fullscreen-button{width:32px;height:32px;margin:4px;bottom:0;right:0;z-index:3;background-image:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAQAAAAAYLlVAAAHvklEQVRo3u1Ze2wURRjftrSU44oviCYa/9D4CAoaX1FjQjT+YzQxJpqoiREfIII81BJRENQKqKW7e6XXFlCQYlBRKi1tKUal4qNFawNI29vX7N21196jd729PuiD23Fmr3u327u927aJf/WbXnO7N/N9v/lm5pv5fUPY5tO3trzVuZ/9hjmUtlSBL8ABYQO4iiCELMJQ6EVVy85uZb9mDqfXx34JDgAbeI6gb6TI35p7/P2yFAkblH70kST/iAj5I+BaggCGAEAWfdueir9bRegblaRYS0OtUa9fpAnbUurUaVcIXoIQRg0LhKPQC4GfXyvOI9KK7Yqylcc7WckLR9JqlJHFMBT3E/RS6mSTEB6Ek0XWfI9eggEoOvlVIJ/IKLsspauPcUyfH45DBbtWn6x9kobFCoJeQjX8yvcPRnW1ZBj7U56j49APhS72DSaXMCXb86nVx4TOPh8cUyCo+rBqOQ5AhuFMAGJfx7D5HmaDYy5hWj61UOtrgCPoxxBi/ZgmADRSfVBwMYWMhZiSfGa1bTwOHL4AHgg4AwAXYXeoc0t7PjFlKSmgdxzvckrDMwMwArvDTBFXgFWmW/8pIoKlbEdDt3NghgAuwRAUvdyHwsLYOjdr3r5gzzuNgAsFlQU+TQCxhYBngRjmtoErzEMos1a+fcLFDyozQFbMTg+ABkKI2yxeZrL3lor1DU52IGF+CgDUogJQWsvjOBD1cZucBSbMz6tYXS+yEb/GfFyf7ikJgBxzVTQePBLvYhD8XKHLmt58eX75ijqBkdQIIKthINZ3JQqrYxIDcHscwIQpxX50wnEw7kAZx0PQy20QCtKZr1hxnGckn2peVqNQrGuyxn6qIZCjcgT1NIg3EhVCwmlKTAQe/nXX3FSTEWTZrGXP1p5zhH2J3sta8yNIcwBGMI6EB0qWkA1NqgeiYegMn+k63+2NQ4jPhTgEsbrzamQuOwlANnmf/dQZ3od2Tv3Ui5nH+2m7s7lX7O/HbkZ/MQBLFQBDqFJUgq7x9oMHi77pbPd6sZpofNbGp04EuhrPXWsA4PGys2c7pMTAJRZzdAyZ5x1N7+2r+cUljoaVTUrjgTDywAAyz1Q5btqaV/LyUa4jMAEhsY9O9AIccaT2QFbJfWW/tDDeSQOIp94Y9EEBsK8SRPEt+442dTnHIujXyJDqATYUkWDXJeZw561Y1QdzS16r5pO2U8W84OBf8OSmDkg7rfTT1W3tvl4tBNW8k13FzsG1ihfvqzntdo9LMBxx2gnybvJw85lu6Ib8t47bVFVF88g1PwiOOISYGuREjl0OkHneIB5uzqWWf8+2+9UBTH2a2HXn57UtDjf0QHEfQS0mV5w7KAT5k+wdWlUfW8gNx9QdfRyOq07kstPHAd0AonaKec/k0wT5wFefdPwsBIGdoOcXL+Qe5ddxDyada6z0xhqRCeGIpjqRyckcCWMD2NGHVwMOX0IvU+iYtJ0vzy5e9M8yfq3wWFpVOy+zbWo4y/t8yDwQ2bVmj2TIe2tq29geL2onethNDgsxXfl0wf5HWjY5ivj3uee5Bebb7bTseeiPjajdVu5FbiExU/k49/9tNyuzMiuzMitJRy2QI+SA7Km2E6bZTq8ky/hpulpSppZQLw0r9eQ0WP/K78mZGjkliEB2fcGZfPccIwjYqu59KuW7Lz/yWNt23g5swhpwjXkIuwu+frj1I84OSoU3wfWpIOj0iHM8eanUlF6+d/NPF0AkgM41zj5ui1lyWjq/cl3jOR6dpfqgS+I+ERal9oInT8wlaCt9NfOU8EHy4YhcUPluo5sf6sNHO8wMA+bIKWkpX12nkNMxlBsIQlHiioSr9L0uy7Ut/PcJYZvwDEEvpladPwyGhRbhIfwTN1GJtFYUahm+WXJK5aM8IUiQU312QbVAP/AdxfwFLoK9BHUPdaS5tQd2Q6GRvR9XwEdu1AsdwzdLTsl59pW1PBNnh8nZBR4tS+rOQ/WtoBv2QOcXmJj8iMnpADqlc/XsvTEn2tfUTWL4ZsgpZd39XO15PTlNzi6Qi6vqmnu7ERMLDznLMTU7eQplSmU4BLsgV8PeReaWvqJ1ojwDcqrNLgA0gN655M1Vx/7sdcPBODVbQp7A5BTTvwEEwVH9XXE16wgZMPwM5NSeRE512YWu5u2H6n/zuJEW/FplxydUeo7Vu0favB1+I4Y/HXKq9R7jbQ24hlWIk/MDystBtHD60zD8qZFTfXZhFGkOorGPGieptLmxlAw/Azndmku/eJRJkNNE1k2W9TpT5Yh0GXpZM4pahp+JnG7PI1+qTpFdmEhSqVk685lSPcM3Q0535JErf+C02YUZZEqnd1+wc/a+YPa+YPa+YEr3BTgQcWog0hRNFFf2shC7hTN9X1C5vh6dJnQJe+1/BUc0AaCJ60fbk3LyMihRFMOdPr5QMJEnKrdUrKsDrBTAzk+jE11cDoh2fHP602kxhJ7xZWrqgjOOozhTNsS/C+ZnOJBeWb6qgeUu4j0RJ+eNdY6jrQlf3d5AFZ/+w+MJjoaCRiWIPuGgbxhdXh8F12W6vN5b+Xcbury+GJ5oaah1pNcDdqHFQt70+2sXqPY97buNy4WyjlJ+F6CFleDKDJfXi75c1raRrei0p9OG9NEcKWwDT/4HecXIWo9QtjoAAAAASUVORK5CYII=);background-size:100% 100%}.presentation:hover .nav-arrow-left,.presentation:hover .nav-arrow-right{opacity:1}.presentation:hover .nav-fullscreen-button{opacity:.8}.presentation-wrapper-fullscreen .nav-fullscreen-button{background-image:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAQAAAAAYLlVAAAH30lEQVRo3u1ZXVBU1x3nghYqILRNMhFNSpFIotMkTvJQx/TFmY5JHtR2al8aM+1TkwdnOn3wJdPmIZ2ahLAfKBqCFtYPFIOIC9jyETOICxI+VBDJ3nvPufuJLCrCLrIGyz05537v3XvvrkqnztRzuJed3fP//3/nf875n//5nYwMpTCU+pnVfH70kra2W1kjuQN5TM7SQ8D6sgfzruZOZpn8TFP7s+s29f2DPsLVgY/B68YQYCbMtDICKWD4u3NN6x9GD0AXPMS+BwszMryJmsspmqrNOriz7TI9PYXuoBBiG+mXk5Wn21ega1lZesTVxwTRNJpC3CTzF39uEoT92Hwr7Y1F0AJCKIaCiDGAkJHhK4ArGVMgDAXzfYX6bx0lrpMXbwRQFGu+j24iGBEhaIp9efU7LYw3NkXM87jixhjCaS2E6kxn0eA29jDYw6008gakHE/XlzF/ZuvAr7Tf29bWNRDzs9g80S1DgCpQ+wrHdvcwHY1I5nmkh0Bc6nz1ZM31QQ7Bf7PPkrmQPDvsW774aLyTQ6CH3SxLEfOeScW8AoGbZP+kTEdbmfNMN6ea56XGWgi29cdaBkJhFEH+lpFVRgBApn1bVd/IUASFEeikN8u915rnpZfghZor8jDYXnX09rC3xR8lmJqBaKQ32F482tI/FUJ30RwKNQ6aeKDirX1XhseiuFUYMZ30JltJ7Qmt84lWuXPTiKsdypNEP1vtKG+n/f+Z0ULgVQhXW09f8kwEsXGEn8DpYTMAbxIAMdzqLl5HY183XewOJZiXXgh/F0DgIy5bEn2XKi9xuS6E/YszcmOhyBBC97yzoe+IYrI+RADABMDQWFRoN4fC970zgflZVaPSqVnkR8xR8POEMFleevjEhQk/r0BQxotHcazunuQavEBNPWDbij1wLSo5+R6Wiis6eF4eVtE8U5YULyrW/rPeGAISCy8CMB8C+9b9KgCNFI/0vRfNJxUMIdkLsiJxalgOgQaARkbbEUvziRB4dS4gxKueMPcA0HlAkEuQFswfszAvQCjFEEI+PB0XE5YDjx4IgCIjRxWemOdx719MuZHYfnb4yPmAf25ecmK6APRDwCvSpMRRKOY9yKxNax+zbz/BjN+JLimAOeQD139ntFMmFce6Y2d7b4QW4hpXqpM63SFQAr8keQ9NLDBn6U0pPVD50vGW/kgQG5IncLqTEBpMQnljIw8O4iRAb7bIZfCOt75eiPlz6lrWLcM5HIiGrACM6ZehGkPuCtuUulPqyoFM5yunzg3eCovmTQoG4B5eZQLgbQzAG7WQFiD0JOYLygg6i6r29tAQTeLoH8OPcb2J/G3XzABsqeq9fG3KVJZojSAOsbUka9KFMkg5n/p8+6VP2CbQBL4Epwzql6DBd9LXAHczBUYZEaDsRdW/6f+EbYZNhvJYA9fgPwkbwW6Yb5Jh9uf9q7il+PRPzxjW5ufPPzvyEyZvwnQh3aD681uLm4ubTDS41/Q9w/yYy2WWOOFfugIpkvcD3SNWIL2tAwmgrKSl/49t/5+UJ+VJeQwKoKBh+NCEoRSBiBAUwERaqY9tIKIptuDCuq517Ws7SttLO6TaLjzk3VXieW60iCkMm5I0E9Toj74q63hBLylr6ywZWMOu4goMNiNMLzxVvWPAznZx7b42eA62JVeuNdDqPwf3MIXG27GjqObXg3bYxXVwbUby8BzX6m+F7WAPXJmUUUAxIfmWJCQxnLnEDOocrrdwQjJqkpA4tlR5Lo/dFNqZyUcQROwhX4GBhn1ZjlfqW76JhFKlZGeHzACQlOzbqKV0CIF28IZpUmpbf8TdN0lyYk1GrmbYmqQUWCelvEZG+YRlEetmX7M8HVSsd7l7BUZLy1SgRz2Y4P8C8+amX0t9NCtzNfWEgnHpYPKQJyNJilcPJuE4fYLe+MBHM55XDgcPeDznFWnlaLYzvaNZcd3x7nAgPi/Zf/TjuXg4Dc/TLnpD6qMZZjU9E4Ra4pf4eB41ZV/15if1xNqjno55U/Y1pXlzigY+FEWjhZDExFdKlPLsQ5JUwJqksoJAPiSZlycQfs9jsXgaNJ0WACH3olhyUacNJcwFCUINZS85ftRj0nvM7cxfnw7GoyjVEAg84ZjcLrgwPu2f09BdCV5gG8UrETH0rHZ+2skE+ShCSVQtYbauNDX09mDSVSRhA6b8gMiUxsSAjUbbT3WfD/hU9lVD1cbInrBXvBgSyGqn56JKVvNITyuWlr9UhwN0UNjlUpDV16OCeRx0N5aX1NR3a3lHmYvHf3cwWT0gk9UVZY7mbm4Sfaej67W8XvkGl7vfH8KbtRldj4dg2/6+keEb5MJHivmEANZAUAZ2gWzLNddkun5vrm3HmaHxGRmCxryG063YeKx6zAMtLyyq/z7eCRHoUHc8PQTFfJD9451MZRV8+IMDv2/2js9EFAjJpOpfs8rXfLOVdYDdXL4JQfFMXRnzHtgHfplwIaZAUHsPgsz7/ryEWPDBssqdBILgBQtO17+CW0FbbCfcD325+u8kCIsEgmiefT+ck3Tf9bfl+37rHvRORdBtFFw0Mp9+Oq1vWfHC4VrPeOD+beL8ACOYT0pMGerjnEO/uPih9yCsBB9orhN08Q6mPBcYJjrPndl19TO2CtrYXb58A/NyQdSV7Es53LL/Cv+y7FLO1ex5Ks0r5v/R5fX/Zfkezyh0SxOzfa0AAAAASUVORK5CYII=)}.screen-reader-text{border:0;clip:rect(1px,1px,1px,1px);-webkit-clip-path:inset(50%);clip-path:inset(50%);height:1px;margin:-1px;overflow:hidden;padding:0;position:absolute!important;width:1px;word-wrap:normal!important}.jetpack-social-navigation ul{display:block;margin:0 0 1.5em;padding:0}.jetpack-social-navigation li{display:inline-block;margin:0;line-height:1}.jetpack-social-navigation a{border:0;height:1em;text-decoration:none;width:1em}.jetpack-social-navigation-svg .icon{color:inherit;fill:currentColor;height:1em;vertical-align:middle;width:1em}.jetpack-social-navigation-genericons a:before{-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;display:inline-block;font-family:Genericons;font-size:1em;font-style:normal;font-weight:400;height:1em;line-height:1;speak:none;text-decoration:inherit;vertical-align:top;width:1em}.jetpack-social-navigation-genericons a:before{content:"\f415"}.jetpack-social-navigation-genericons a[href*="codepen.io"]:before{content:"\f216"}.jetpack-social-navigation-genericons a[href*="digg.com"]:before{content:"\f221"}.jetpack-social-navigation-genericons a[href*="dribbble.com"]:before{content:"\f201"}.jetpack-social-navigation-genericons a[href*="dropbox.com"]:before{content:"\f225"}.jetpack-social-navigation-genericons a[href*="mailto:"]:before{content:"\f410"}.jetpack-social-navigation-genericons a[href*="facebook.com"]:before{content:"\f203"}.jetpack-social-navigation-genericons a[href*="flickr.com"]:before{content:"\f211"}.jetpack-social-navigation-genericons a[href*="foursquare.com"]:before{content:"\f226"}.jetpack-social-navigation-genericons a[href*="github.com"]:before{content:"\f200"}.jetpack-social-navigation-genericons a[href*="plus.google.com"]:before{content:"\f206"}.jetpack-social-navigation-genericons a[href*="instagram.com"]:before{content:"\f215"}.jetpack-social-navigation-genericons a[href*="linkedin.com"]:before{content:"\f208"}.jetpack-social-navigation-genericons a[href*="path.com"]:before{content:"\f219"}.jetpack-social-navigation-genericons a[href*="pinterest."]:before{content:"\f210"}.jetpack-social-navigation-genericons a[href*="getpocket.com"]:before{content:"\f224"}.jetpack-social-navigation-genericons a[href*="polldaddy.com"]:before{content:"\f217"}.jetpack-social-navigation-genericons a[href*="reddit.com"]:before{content:"\f222"}.jetpack-social-navigation-genericons a[href$="/feed/"]:before{content:"\f413"}.jetpack-social-navigation-genericons a[href*="skype:"]:before{content:"\f220"}.jetpack-social-navigation-genericons a[href*="spotify.com"]:before{content:"\f515"}.jetpack-social-navigation-genericons a[href*="stumbleupon.com"]:before{content:"\f223"}.jetpack-social-navigation-genericons a[href*="tumblr.com"]:before{content:"\f214"}.jetpack-social-navigation-genericons a[href*="twitch.tv"]:before{content:"\f516"}.jetpack-social-navigation-genericons a[href*="twitter.com"]:before{content:"\f202"}.jetpack-social-navigation-genericons a[href*="vimeo.com"]:before{content:"\f212"}.jetpack-social-navigation-genericons a[href*="vine.co"]:before{content:"\f517"}.jetpack-social-navigation-genericons a[href*="wordpress.com"]:before,.jetpack-social-navigation-genericons a[href*="wordpress.org"]:before{content:"\f205"}.jetpack-social-navigation-genericons a[href*="youtube.com"]:before{content:"\f213"}@keyframes fadeIn{0%{opacity:0;visibility:hidden}to{opacity:1;visibility:visible}}.screen-reader-text{border:0;clip:rect(1px,1px,1px,1px);-webkit-clip-path:inset(50%);clip-path:inset(50%);height:1px;margin:-1px;overflow:hidden;padding:0;position:absolute!important;width:1px;word-wrap:normal!important}</style><link rel="stylesheet" media="all" onload="this.media=&#39;all&#39;" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/3d1bea95f8f0.post.used.css"><link rel="preload" href="https://randomnerdtutorials.com/wp-content/themes/generatepress/assets/fonts/generatepress.woff2" as="font" type="font/woff2" crossorigin="">

		<!-- All in One SEO 4.1.1.1 -->
		<meta name="description" content="The ESP32 can act as a Wi-Fi station, as an AP (Access Point), or both. In this tutorial you&#39;ll set the ESP32 as an access point using the Arduino IDE.">
		<meta name="keywords" content="esp32 softap,esp32 ap web server,esp32 soft access point code,esp32 access point arduino ide,esp32 softap arduino ide,esp32 ap access point for web server">
		<link rel="canonical" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/">
		<meta property="og:site_name" content="Random Nerd Tutorials">
		<meta property="og:type" content="article">
		<meta property="og:title" content="ESP32 Access Point (AP) for Web Server | Random Nerd Tutorials">
		<meta property="og:description" content="The ESP32 can act as a Wi-Fi station, as an AP (Access Point), or both. In this tutorial you&#39;ll set the ESP32 as an access point using the Arduino IDE.">
		<meta property="og:url" content="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/">
		<meta property="og:image" content="https://randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg">
		<meta property="og:image:secure_url" content="https://randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg">
		<meta property="og:image:width" content="1280">
		<meta property="og:image:height" content="720">
		<meta property="article:published_time" content="2018-08-09T09:08:27Z">
		<meta property="article:modified_time" content="2019-04-23T09:12:43Z">
		<meta name="twitter:card" content="summary">
		<meta name="twitter:domain" content="randomnerdtutorials.com">
		<meta name="twitter:title" content="ESP32 Access Point (AP) for Web Server | Random Nerd Tutorials">
		<meta name="twitter:description" content="The ESP32 can act as a Wi-Fi station, as an AP (Access Point), or both. In this tutorial you&#39;ll set the ESP32 as an access point using the Arduino IDE.">
		<meta name="twitter:image" content="https://randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg">
		<meta name="google" content="nositelinkssearchbox">
		<script type="text/javascript" async="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/analytics.js.download"></script><script type="application/ld+json" class="aioseo-schema">
			{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebSite","@id":"https:\/\/randomnerdtutorials.com\/#website","url":"https:\/\/randomnerdtutorials.com\/","name":"Random Nerd Tutorials","description":"Learn ESP8266, ESP32, Arduino, and Raspberry Pi","publisher":{"@id":"https:\/\/randomnerdtutorials.com\/#organization"}},{"@type":"Organization","@id":"https:\/\/randomnerdtutorials.com\/#organization","name":"Random Nerd Tutorials","url":"https:\/\/randomnerdtutorials.com\/"},{"@type":"BreadcrumbList","@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#breadcrumblist","itemListElement":[{"@type":"ListItem","@id":"https:\/\/randomnerdtutorials.com\/#listItem","position":"1","item":{"@id":"https:\/\/randomnerdtutorials.com\/#item","name":"Home","description":"Random Nerd Tutorials helps makers, hobbyists and engineers build electronics projects. We make projects with: ESP32, ESP8266, Arduino, Raspberry Pi, Home Automation and Internet of Things. If you want to learn electronics and programming, you're in the right place.","url":"https:\/\/randomnerdtutorials.com\/"},"nextItem":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#listItem"},{"@type":"ListItem","@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#listItem","position":"2","item":{"@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#item","name":"How to Set an ESP32 Access Point (AP) for Web Server","description":"The ESP32 can act as a Wi-Fi station, as an AP (Access Point), or both. In this tutorial you'll set the ESP32 as an access point using the Arduino IDE.","url":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/"},"previousItem":"https:\/\/randomnerdtutorials.com\/#listItem"}]},{"@type":"Person","@id":"https:\/\/randomnerdtutorials.com\/author\/sara-santos\/#author","url":"https:\/\/randomnerdtutorials.com\/author\/sara-santos\/","name":"Sara Santos","image":{"@type":"ImageObject","@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#authorImage","url":"https:\/\/secure.gravatar.com\/avatar\/25e3da92f25bc3fde695d9c0d92207b0?s=96&d=mm&r=g","width":"96","height":"96","caption":"Sara Santos"}},{"@type":"WebPage","@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#webpage","url":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/","name":"ESP32 Access Point (AP) for Web Server | Random Nerd Tutorials","description":"The ESP32 can act as a Wi-Fi station, as an AP (Access Point), or both. In this tutorial you'll set the ESP32 as an access point using the Arduino IDE.","inLanguage":"en-US","isPartOf":{"@id":"https:\/\/randomnerdtutorials.com\/#website"},"breadcrumb":{"@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#breadcrumblist"},"author":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#author","creator":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#author","image":{"@type":"ImageObject","@id":"https:\/\/randomnerdtutorials.com\/#mainImage","url":"https:\/\/i0.wp.com\/randomnerdtutorials.com\/wp-content\/uploads\/2018\/07\/ESP32-access-point-1.jpg?fit=1280%2C720&quality=100&strip=all&ssl=1","width":"1280","height":"720"},"primaryImageOfPage":{"@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#mainImage"},"datePublished":"2018-08-09T09:08:27+00:00","dateModified":"2019-04-23T09:12:43+00:00"},{"@type":"Article","@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#article","name":"ESP32 Access Point (AP) for Web Server | Random Nerd Tutorials","description":"The ESP32 can act as a Wi-Fi station, as an AP (Access Point), or both. In this tutorial you'll set the ESP32 as an access point using the Arduino IDE.","headline":"How to Set an ESP32 Access Point (AP) for Web Server","author":{"@id":"https:\/\/randomnerdtutorials.com\/author\/sara-santos\/#author"},"publisher":{"@id":"https:\/\/randomnerdtutorials.com\/#organization"},"datePublished":"2018-08-09T09:08:27+00:00","dateModified":"2019-04-23T09:12:43+00:00","commentCount":"94","articleSection":"ESP32, ESP32, ESP32 Arduino IDE, ESP32 Projects, Project","mainEntityOfPage":{"@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#webpage"},"isPartOf":{"@id":"https:\/\/randomnerdtutorials.com\/esp32-access-point-ap-web-server\/#webpage"},"image":{"@type":"ImageObject","@id":"https:\/\/randomnerdtutorials.com\/#articleImage","url":"https:\/\/i0.wp.com\/randomnerdtutorials.com\/wp-content\/uploads\/2018\/07\/ESP32-access-point-1.jpg?fit=1280%2C720&quality=100&strip=all&ssl=1","width":"1280","height":"720"}}]}
		</script>
		<!-- All in One SEO -->

<link rel="dns-prefetch" href="https://scripts.mediavine.com/">
<link rel="dns-prefetch" href="https://s.w.org/">
<link rel="dns-prefetch" href="https://v0.wordpress.com/">
<link rel="dns-prefetch" href="https://i0.wp.com/">
<link rel="dns-prefetch" href="https://i1.wp.com/">
<link rel="dns-prefetch" href="https://i2.wp.com/">
<link rel="alternate" type="application/rss+xml" title="Random Nerd Tutorials » Feed" href="https://randomnerdtutorials.com/feed/">
<link rel="alternate" type="application/rss+xml" title="Random Nerd Tutorials » Comments Feed" href="https://randomnerdtutorials.com/comments/feed/">
<link rel="alternate" type="application/rss+xml" title="Random Nerd Tutorials » How to Set an ESP32 Access Point (AP) for Web Server Comments Feed" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/feed/">
		<script>
			window._wpemojiSettings = {"baseUrl":"https:\/\/s.w.org\/images\/core\/emoji\/13.0.1\/72x72\/","ext":".png","svgUrl":"https:\/\/s.w.org\/images\/core\/emoji\/13.0.1\/svg\/","svgExt":".svg","source":{"concatemoji":"https:\/\/randomnerdtutorials.com\/wp-includes\/js\/wp-emoji-release.min.js?ver=5.7.2"}};
			!function(e,a,t){var n,r,o,i=a.createElement("canvas"),p=i.getContext&&i.getContext("2d");function s(e,t){var a=String.fromCharCode;p.clearRect(0,0,i.width,i.height),p.fillText(a.apply(this,e),0,0);e=i.toDataURL();return p.clearRect(0,0,i.width,i.height),p.fillText(a.apply(this,t),0,0),e===i.toDataURL()}function c(e){var t=a.createElement("script");t.src=e,t.defer=t.type="text/javascript",a.getElementsByTagName("head")[0].appendChild(t)}for(o=Array("flag","emoji"),t.supports={everything:!0,everythingExceptFlag:!0},r=0;r<o.length;r++)t.supports[o[r]]=function(e){if(!p||!p.fillText)return!1;switch(p.textBaseline="top",p.font="600 32px Arial",e){case"flag":return s([127987,65039,8205,9895,65039],[127987,65039,8203,9895,65039])?!1:!s([55356,56826,55356,56819],[55356,56826,8203,55356,56819])&&!s([55356,57332,56128,56423,56128,56418,56128,56421,56128,56430,56128,56423,56128,56447],[55356,57332,8203,56128,56423,8203,56128,56418,8203,56128,56421,8203,56128,56430,8203,56128,56423,8203,56128,56447]);case"emoji":return!s([55357,56424,8205,55356,57212],[55357,56424,8203,55356,57212])}return!1}(o[r]),t.supports.everything=t.supports.everything&&t.supports[o[r]],"flag"!==o[r]&&(t.supports.everythingExceptFlag=t.supports.everythingExceptFlag&&t.supports[o[r]]);t.supports.everythingExceptFlag=t.supports.everythingExceptFlag&&!t.supports.flag,t.DOMReady=!1,t.readyCallback=function(){t.DOMReady=!0},t.supports.everything||(n=function(){t.readyCallback()},a.addEventListener?(a.addEventListener("DOMContentLoaded",n,!1),e.addEventListener("load",n,!1)):(e.attachEvent("onload",n),a.attachEvent("onreadystatechange",function(){"complete"===a.readyState&&t.readyCallback()})),(n=t.source||{}).concatemoji?c(n.concatemoji):n.wpemoji&&n.twemoji&&(c(n.twemoji),c(n.wpemoji)))}(window,document,window._wpemojiSettings);
		</script><script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/wp-emoji-release.min.js.download" type="text/javascript" defer=""></script>
		<style>
img.wp-smiley,
img.emoji {
	display: inline !important;
	border: none !important;
	box-shadow: none !important;
	height: 1em !important;
	width: 1em !important;
	margin: 0 .07em !important;
	vertical-align: -0.1em !important;
	background: none !important;
	padding: 0 !important;
}
</style>
	<link rel="stylesheet" id="wp-block-library-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/b5d1e2c87b60.style.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/b5d1e2c87b60.style.min.css">
<style id="wp-block-library-inline-css">
.has-text-align-justify{text-align:justify;}
</style>
<link rel="stylesheet" id="generate-style-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/3086e2c40c5b.all.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/3086e2c40c5b.all.min.css">
<style id="generate-style-inline-css">
body{background-color:#ffffff;color:#3a3a3a;}a{color:#1b78e2;}a:visited{color:#1b78e2;}a:hover, a:focus, a:active{color:#000000;}body .grid-container{max-width:1380px;}.wp-block-group__inner-container{max-width:1380px;margin-left:auto;margin-right:auto;}.navigation-search{position:absolute;left:-99999px;pointer-events:none;visibility:hidden;z-index:20;width:100%;top:0;transition:opacity 100ms ease-in-out;opacity:0;}.navigation-search.nav-search-active{left:0;right:0;pointer-events:auto;visibility:visible;opacity:1;}.navigation-search input[type="search"]{outline:0;border:0;vertical-align:bottom;line-height:1;opacity:0.9;width:100%;z-index:20;border-radius:0;-webkit-appearance:none;height:60px;}.navigation-search input::-ms-clear{display:none;width:0;height:0;}.navigation-search input::-ms-reveal{display:none;width:0;height:0;}.navigation-search input::-webkit-search-decoration, .navigation-search input::-webkit-search-cancel-button, .navigation-search input::-webkit-search-results-button, .navigation-search input::-webkit-search-results-decoration{display:none;}.main-navigation li.search-item{z-index:21;}li.search-item.active{transition:opacity 100ms ease-in-out;}.nav-left-sidebar .main-navigation li.search-item.active,.nav-right-sidebar .main-navigation li.search-item.active{width:auto;display:inline-block;float:right;}.gen-sidebar-nav .navigation-search{top:auto;bottom:0;}body, button, input, select, textarea{font-family:Helvetica;font-size:18px;}body{line-height:1.5;}p{margin-bottom:1.4em;}.entry-content > [class*="wp-block-"]:not(:last-child){margin-bottom:1.4em;}.main-title{font-size:45px;}.main-navigation .main-nav ul ul li a{font-size:14px;}.widget-title{font-weight:600;}.sidebar .widget, .footer-widgets .widget{font-size:17px;}button:not(.menu-toggle),html input[type="button"],input[type="reset"],input[type="submit"],.button,.wp-block-button .wp-block-button__link{font-size:20px;}h1{font-weight:600;font-size:36px;margin-bottom:14px;}h2{font-weight:600;font-size:36px;line-height:1.3em;margin-bottom:18px;}h3{font-weight:600;line-height:1.3em;margin-bottom:10px;}h4{font-weight:600;font-size:20px;}h5{font-size:inherit;}@media (max-width:768px){.main-title{font-size:30px;}h1{font-size:27px;}h2{font-size:27px;}}.top-bar{background-color:#636363;color:#ffffff;}.top-bar a{color:#ffffff;}.top-bar a:hover{color:#303030;}.site-header{background-color:#ffffff;color:#3a3a3a;}.site-header a{color:#3a3a3a;}.main-title a,.main-title a:hover{color:#222222;}.site-description{color:#757575;}.main-navigation,.main-navigation ul ul{background-color:#2f4468;}.main-navigation .main-nav ul li a,.menu-toggle, .main-navigation .menu-bar-items{color:#ffffff;}.main-navigation .main-nav ul li:hover > a,.main-navigation .main-nav ul li:focus > a, .main-navigation .main-nav ul li.sfHover > a, .main-navigation .menu-bar-item:hover > a, .main-navigation .menu-bar-item.sfHover > a{color:#dee5ed;background-color:#2f4468;}button.menu-toggle:hover,button.menu-toggle:focus,.main-navigation .mobile-bar-items a,.main-navigation .mobile-bar-items a:hover,.main-navigation .mobile-bar-items a:focus{color:#ffffff;}.main-navigation .main-nav ul li[class*="current-menu-"] > a{color:#ffffff;background-color:rgba(10,10,10,0.31);}.main-navigation .main-nav ul li[class*="current-menu-"] > a:hover,.main-navigation .main-nav ul li[class*="current-menu-"].sfHover > a{color:#ffffff;background-color:rgba(10,10,10,0.31);}.navigation-search input[type="search"],.navigation-search input[type="search"]:active, .navigation-search input[type="search"]:focus, .main-navigation .main-nav ul li.search-item.active > a, .main-navigation .menu-bar-items .search-item.active > a{color:#dee5ed;background-color:#2f4468;}.main-navigation ul ul{background-color:#3f3f3f;}.main-navigation .main-nav ul ul li a{color:#ffffff;}.main-navigation .main-nav ul ul li:hover > a,.main-navigation .main-nav ul ul li:focus > a,.main-navigation .main-nav ul ul li.sfHover > a{color:#ffffff;background-color:#4f4f4f;}.main-navigation .main-nav ul ul li[class*="current-menu-"] > a{color:#ffffff;background-color:#4f4f4f;}.main-navigation .main-nav ul ul li[class*="current-menu-"] > a:hover,.main-navigation .main-nav ul ul li[class*="current-menu-"].sfHover > a{color:#ffffff;background-color:#4f4f4f;}.separate-containers .inside-article, .separate-containers .comments-area, .separate-containers .page-header, .one-container .container, .separate-containers .paging-navigation, .inside-page-header{background-color:#ffffff;}.entry-title a{color:#2f4468;}.entry-title a:hover{color:#0a0000;}.entry-meta{color:#878787;}.entry-meta a{color:#727272;}.entry-meta a:hover{color:#0a0101;}.sidebar .widget{background-color:#ffffff;}.sidebar .widget .widget-title{color:#000000;}.footer-widgets{color:#ffffff;background-color:#2f4468;}.footer-widgets a{color:#ffffff;}.footer-widgets .widget-title{color:#ffffff;}.site-info{color:#2f4468;}.site-info a{color:#2f4468;}.site-info a:hover{color:#0a0a0a;}.footer-bar .widget_nav_menu .current-menu-item a{color:#0a0a0a;}input[type="text"],input[type="email"],input[type="url"],input[type="password"],input[type="search"],input[type="tel"],input[type="number"],textarea,select{color:#666666;background-color:#fafafa;border-color:#cccccc;}input[type="text"]:focus,input[type="email"]:focus,input[type="url"]:focus,input[type="password"]:focus,input[type="search"]:focus,input[type="tel"]:focus,input[type="number"]:focus,textarea:focus,select:focus{color:#666666;background-color:#ffffff;border-color:#bfbfbf;}button,html input[type="button"],input[type="reset"],input[type="submit"],a.button,a.wp-block-button__link:not(.has-background){color:#ffffff;background-color:#2f4468;}button:hover,html input[type="button"]:hover,input[type="reset"]:hover,input[type="submit"]:hover,a.button:hover,button:focus,html input[type="button"]:focus,input[type="reset"]:focus,input[type="submit"]:focus,a.button:focus,a.wp-block-button__link:not(.has-background):active,a.wp-block-button__link:not(.has-background):focus,a.wp-block-button__link:not(.has-background):hover{color:#ffffff;background-color:#0c2c68;}a.generate-back-to-top{background-color:rgba( 0,0,0,0.4 );color:#ffffff;}a.generate-back-to-top:hover,a.generate-back-to-top:focus{background-color:rgba( 0,0,0,0.6 );color:#ffffff;}@media (max-width: 768px){.main-navigation .menu-bar-item:hover > a, .main-navigation .menu-bar-item.sfHover > a{background:none;color:#ffffff;}}.inside-top-bar{padding:10px;}.inside-header{padding:0px;}.separate-containers .inside-article, .separate-containers .comments-area, .separate-containers .page-header, .separate-containers .paging-navigation, .one-container .site-content, .inside-page-header, .wp-block-group__inner-container{padding:10px 8px 8px 8px;}.entry-content .alignwide, body:not(.no-sidebar) .entry-content .alignfull{margin-left:-8px;width:calc(100% + 16px);max-width:calc(100% + 16px);}.one-container.right-sidebar .site-main,.one-container.both-right .site-main{margin-right:8px;}.one-container.left-sidebar .site-main,.one-container.both-left .site-main{margin-left:8px;}.one-container.both-sidebars .site-main{margin:0px 8px 0px 8px;}.separate-containers .widget, .separate-containers .site-main > *, .separate-containers .page-header, .widget-area .main-navigation{margin-bottom:8px;}.separate-containers .site-main{margin:8px;}.both-right.separate-containers .inside-left-sidebar{margin-right:4px;}.both-right.separate-containers .inside-right-sidebar{margin-left:4px;}.both-left.separate-containers .inside-left-sidebar{margin-right:4px;}.both-left.separate-containers .inside-right-sidebar{margin-left:4px;}.separate-containers .page-header-image, .separate-containers .page-header-contained, .separate-containers .page-header-image-single, .separate-containers .page-header-content-single{margin-top:8px;}.separate-containers .inside-right-sidebar, .separate-containers .inside-left-sidebar{margin-top:8px;margin-bottom:8px;}.rtl .menu-item-has-children .dropdown-menu-toggle{padding-left:20px;}.rtl .main-navigation .main-nav ul li.menu-item-has-children > a{padding-right:20px;}.widget-area .widget{padding:10px 2px 4px 2px;}.site-info{padding:20px;}@media (max-width:768px){.separate-containers .inside-article, .separate-containers .comments-area, .separate-containers .page-header, .separate-containers .paging-navigation, .one-container .site-content, .inside-page-header, .wp-block-group__inner-container{padding:30px;}.site-info{padding-right:10px;padding-left:10px;}.entry-content .alignwide, body:not(.no-sidebar) .entry-content .alignfull{margin-left:-30px;width:calc(100% + 60px);max-width:calc(100% + 60px);}}/* End cached CSS */@media (max-width: 768px){.main-navigation .menu-toggle,.main-navigation .mobile-bar-items,.sidebar-nav-mobile:not(#sticky-placeholder){display:block;}.main-navigation ul,.gen-sidebar-nav{display:none;}[class*="nav-float-"] .site-header .inside-header > *{float:none;clear:both;}}
.dynamic-author-image-rounded{border-radius:100%;}.dynamic-featured-image, .dynamic-author-image{vertical-align:middle;}.one-container.blog .dynamic-content-template:not(:last-child), .one-container.archive .dynamic-content-template:not(:last-child){padding-bottom:0px;}.dynamic-entry-excerpt > p:last-child{margin-bottom:0px;}
.main-navigation .navigation-logo img {height:60px;}@media (max-width: 1390px) {.main-navigation .navigation-logo.site-logo {margin-left:0;}body.sticky-menu-logo.nav-float-left .main-navigation .site-logo.navigation-logo {margin-right:0;}}.main-navigation .main-nav ul li a,.menu-toggle,.main-navigation .mobile-bar-items a{transition: line-height 300ms ease}.main-navigation.toggled .main-nav > ul{background-color: #2f4468}
</style>
<link rel="stylesheet" id="generate-font-icons-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/78ce964ac72d.font-icons.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/78ce964ac72d.font-icons.min.css">
<link rel="stylesheet" id="generate-child-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/273667da91ad.style.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/273667da91ad.style.css">
<link rel="stylesheet" id="elementor-icons-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/809fa83187a5.elementor-icons.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/809fa83187a5.elementor-icons.min.css">
<link rel="stylesheet" id="elementor-animations-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/4601ba550444.animations.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/4601ba550444.animations.min.css">
<link rel="stylesheet" id="elementor-frontend-legacy-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/381eed08d61d.frontend-legacy.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/381eed08d61d.frontend-legacy.min.css">
<link rel="stylesheet" id="elementor-frontend-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/c2268583167c.frontend.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/c2268583167c.frontend.min.css">
<style id="elementor-frontend-inline-css">
@font-face{font-family:eicons;src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.eot?5.10.0);src:url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.eot?5.10.0#iefix) format("embedded-opentype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.woff2?5.10.0) format("woff2"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.woff?5.10.0) format("woff"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.ttf?5.10.0) format("truetype"),url(https://randomnerdtutorials.com/wp-content/plugins/elementor/assets/lib/eicons/fonts/eicons.svg?5.10.0#eicon) format("svg");font-weight:400;font-style:normal}
</style>
<link rel="stylesheet" id="elementor-post-94299-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/281b612b521e.post-94299.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/281b612b521e.post-94299.css">
<link rel="stylesheet" id="elementor-pro-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/db4de5dd3799.frontend.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/db4de5dd3799.frontend.min.css">
<link rel="stylesheet" id="font-awesome-5-all-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/b227b1617a17.all.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/b227b1617a17.all.min.css">
<link rel="stylesheet" id="font-awesome-4-shim-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/0a121a1f354d.v4-shims.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/0a121a1f354d.v4-shims.min.css">
<link rel="stylesheet" id="elementor-post-83058-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/bcfb211601fd.post-83058.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/bcfb211601fd.post-83058.css">
<link rel="stylesheet" id="generate-sticky-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/858f6e0503fe.sticky.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/858f6e0503fe.sticky.min.css">
<link rel="stylesheet" id="generate-menu-logo-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/c1185c7ce5bc.menu-logo.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/c1185c7ce5bc.menu-logo.min.css">
<style id="generate-menu-logo-inline-css">
@media (max-width: 768px){.sticky-menu-logo .navigation-stick:not(.mobile-header-navigation) .menu-toggle,.menu-logo .main-navigation:not(.mobile-header-navigation) .menu-toggle{display:inline-block;clear:none;width:auto;float:right;}.sticky-menu-logo .navigation-stick:not(.mobile-header-navigation) .mobile-bar-items,.menu-logo .main-navigation:not(.mobile-header-navigation) .mobile-bar-items{position:relative;float:right;}.regular-menu-logo .main-navigation:not(.navigation-stick):not(.mobile-header-navigation) .menu-toggle{display:inline-block;clear:none;width:auto;float:right;}.regular-menu-logo .main-navigation:not(.navigation-stick):not(.mobile-header-navigation) .mobile-bar-items{position:relative;float:right;}body[class*="nav-float-"].menu-logo-enabled:not(.sticky-menu-logo) .main-navigation .main-nav{display:block;}.sticky-menu-logo.nav-float-left .navigation-stick:not(.mobile-header-navigation) .menu-toggle,.menu-logo.nav-float-left .main-navigation:not(.mobile-header-navigation) .menu-toggle,.regular-menu-logo.nav-float-left .main-navigation:not(.navigation-stick):not(.mobile-header-navigation) .menu-toggle{float:left;}}
</style>
<link rel="stylesheet" id="google-fonts-1-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/3160f4c8d110.2b647acd5e5d.google-font.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/3160f4c8d110.2b647acd5e5d.google-font.css">
<link rel="stylesheet" id="jetpack_css-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/64eed41abd97.jetpack.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/64eed41abd97.jetpack.css">
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/jquery.min.js.download" id="jquery-core-js"></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/jquery-migrate.min.js.download" id="jquery-migrate-js"></script>
<script async="async" data-noptimize="1" data-cfasync="false" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/random-nerd-tutorials.js.download" id="mv-script-wrapper-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/v4-shims.min.js.download" id="font-awesome-4-shim-js" defer=""></script>
<link rel="https://api.w.org/" href="https://randomnerdtutorials.com/wp-json/"><link rel="alternate" type="application/json" href="https://randomnerdtutorials.com/wp-json/wp/v2/posts/67766"><link rel="EditURI" type="application/rsd+xml" title="RSD" href="https://randomnerdtutorials.com/xmlrpc.php?rsd">
<link rel="wlwmanifest" type="application/wlwmanifest+xml" href="https://randomnerdtutorials.com/wp-includes/wlwmanifest.xml"> 
<meta name="generator" content="WordPress 5.7.2">
<link rel="shortlink" href="https://randomnerdtutorials.com/?p=67766">
<link rel="alternate" type="application/json+oembed" href="https://randomnerdtutorials.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Frandomnerdtutorials.com%2Fesp32-access-point-ap-web-server%2F">
<link rel="alternate" type="text/xml+oembed" href="https://randomnerdtutorials.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Frandomnerdtutorials.com%2Fesp32-access-point-ap-web-server%2F&amp;format=xml">
<style>img{height:auto}</style><meta name="viewport" content="width=device-width, initial-scale=1"><!-- Global site tag (gtag.js) - Google Analytics -->
<script async="" data-lazy-src="https://www.googletagmanager.com/gtag/js?id=UA-41273278-2" data-lazy-method="interaction" data-lazy-attributes="src" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/js"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-41273278-2');
</script>
<style>
@media ( min-width: 782px ) {
  .skip-link {
    display:none;
  }
}
.is-logo-image {
width: 145px;
height: 60px;
}
.rntn-top-menu {
background: #edeff3;
border-radius: 4px;
padding: 4px 8px;
margin: 4px;
}
.rnt-menu-top-links a {
text-decoration: none;
color: #3a3a3a ;
}
.rnt-menu-top-links a:hover { text-decoration: underline; color: #3a3a3a; }
</style><link rel="icon" href="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/03/n-favicon-2018.png?fit=16%2C16&amp;quality=100&amp;strip=all&amp;ssl=1" sizes="32x32">
<link rel="icon" href="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/03/n-favicon-2018.png?fit=16%2C16&amp;quality=100&amp;strip=all&amp;ssl=1" sizes="192x192">
<link rel="apple-touch-icon" href="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/03/n-favicon-2018.png?fit=16%2C16&amp;quality=100&amp;strip=all&amp;ssl=1">
<meta name="msapplication-TileImage" content="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/03/n-favicon-2018.png?fit=16%2C16&amp;quality=100&amp;strip=all&amp;ssl=1">
<link rel="prefetch" href="https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/"><link rel="prefetch" href="https://randomnerdtutorials.com/esp32-static-fixed-ip-address-arduino-ide/"><link rel="prefetch" href="https://randomnerdtutorials.com/projects/"><link rel="prefetch" href="https://randomnerdtutorials.com/projects-esp32-esp8266-micropython/"><link rel="prefetch" href="https://randomnerdtutorials.com/"><link rel="prefetch" href="https://randomnerdtutorials.com/esp32-web-server-arduino-ide/"><link rel="prefetch" href="https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-mac-and-linux-instructions/"><link rel="prefetch" href="https://randomnerdtutorials.com/build-web-servers-esp32-esp8266-ebook/"><link rel="prefetch" href="https://randomnerdtutorials.com/learn-esp32-with-arduino-ide/"><link rel="prefetch" href="https://randomnerdtutorials.com/esp32-cam-projects-ebook/"><link rel="prefetch" href="https://randomnerdtutorials.com/micropython-programming-with-esp32-and-esp8266/"><link rel="prefetch" href="https://randomnerdtutorials.com/courses/"><link rel="prefetch" href="https://randomnerdtutorials.com/contact"></head>

<body data-rsssl="1" class="post-template-default single single-post postid-67766 single-format-standard wp-embed-responsive post-image-above-header post-image-aligned-center sticky-menu-no-transition sticky-enabled menu-logo menu-logo-enabled both-sticky-menu both-sidebars nav-above-header separate-containers fluid-header active-footer-widgets-0 nav-search-enabled nav-aligned-center header-aligned-center dropdown-hover featured-image-active elementor-default elementor-kit-94299 elementor-page-82536 e--ua-blink e--ua-chrome e--ua-webkit vsc-initialized dialog-body dialog-lightbox-body dialog-container dialog-lightbox-container using-mouse" itemtype="https://schema.org/Blog" itemscope="" data-elementor-device-mode="desktop" data-new-gr-c-s-check-loaded="14.1024.0" data-gr-ext-installed="">
	<a class="screen-reader-text skip-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#content" title="Skip to content">Skip to content</a>		<nav id="sticky-navigation" class="auto-hide-sticky main-navigation sub-menu-right stuckElement is_stuck navigation-stick navigation-clone sticky-navigation-transition" itemtype="https://schema.org/SiteNavigationElement" itemscope="" style="z-index: 100; margin-top: 0px; position: fixed; top: 0px;">
			<div class="inside-navigation grid-container grid-parent">
				<div class="site-logo sticky-logo navigation-logo">
					<a href="https://randomnerdtutorials.com/" title="Random Nerd Tutorials" rel="home">
						<img src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/logornt.png" alt="Random Nerd Tutorials" class="is-logo-image" loading="eager" width="250" height="80">
					</a>
				</div><form method="get" class="search-form navigation-search" action="https://randomnerdtutorials.com/">
					<input type="search" class="search-field" value="" name="s" title="Search">
				</form>		<div class="mobile-bar-items">
						<span class="search-item">
				<a aria-label="Open Search Bar" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#">
									</a>
			</span>
		</div>
						<button class="menu-toggle" aria-controls="primary-menu" aria-expanded="false">
					<span class="mobile-menu">Menu</span>				</button>
				<div id="primary-menu" class="main-nav"><ul id="menu-newtop" class=" menu sf-menu"><li id="menu-item-20487" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20487"><a href="https://randomnerdtutorials.com/download">Free eBooks</a></li>
<li id="menu-item-20484" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20484"><a href="https://randomnerdtutorials.com/about">About</a></li>
<li id="menu-item-20485" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20485"><a href="https://randomnerdtutorials.com/contact">Contact</a></li>
<li id="menu-item-68854" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-68854"><a target="_blank" rel="noopener" href="https://rntlab.com/login">Courses Login</a></li>
<li id="menu-item-20483" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-20483"><a href="https://randomnerdtutorials.com/courses/"><strong>Get Courses</strong><span role="presentation" class="dropdown-menu-toggle"></span></a>
<ul class="sub-menu">
	<li id="menu-item-40154" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40154"><a href="https://randomnerdtutorials.com/courses/"><strong>All eBooks &amp; Courses</strong></a></li>
	<li id="menu-item-100940" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-100940"><a href="https://randomnerdtutorials.com/build-web-servers-esp32-esp8266-ebook/"><strong>Build Web Servers with ESP32 and ESP8266</strong></a></li>
	<li id="menu-item-69105" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-69105"><a href="https://randomnerdtutorials.com/learn-esp32-with-arduino-ide/">Learn ESP32 with Arduino IDE</a></li>
	<li id="menu-item-96038" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-96038"><a href="https://randomnerdtutorials.com/esp32-cam-projects-ebook/">Build ESP32-CAM Projects</a></li>
	<li id="menu-item-83302" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-83302"><a href="https://randomnerdtutorials.com/micropython-programming-with-esp32-and-esp8266/">MicroPython Programming with ESP32 and ESP8266</a></li>
	<li id="menu-item-40149" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40149"><a href="https://randomnerdtutorials.com/home-automation-using-esp8266/">Home Automation Using ESP8266</a></li>
	<li id="menu-item-40150" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40150"><a href="https://randomnerdtutorials.com/build-a-home-automation-system-for-100/">Build a Home Automation System for $100</a></li>
	<li id="menu-item-40151" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40151"><a href="https://randomnerdtutorials.com/arduino-step-by-step-projects/">Arduino Step-by-step Projects</a></li>
	<li id="menu-item-40153" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40153"><a href="https://randomnerdtutorials.com/android-apps-for-arduino-with-mit-app-inventor-2/">Android Apps For Arduino</a></li>
	<li id="menu-item-40152" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40152"><a href="https://randomnerdtutorials.com/electronics-for-beginners/">Electronics For Beginners</a></li>
</ul>
</li>
<li class="search-item menu-item-align-right"><a aria-label="Open Search Bar" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#"></a></li></ul></div>			</div>
		</nav><nav id="sticky-placeholder" class="auto-hide-sticky main-navigation sub-menu-right is_stuck navigation-stick navigation-clone sticky-navigation-transition" aria-hidden="true" style="visibility: hidden;">
			<div class="inside-navigation grid-container grid-parent">
				<div class="site-logo sticky-logo navigation-logo">
					<a href="https://randomnerdtutorials.com/" title="Random Nerd Tutorials" rel="home">
						<img src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/logornt.png" alt="Random Nerd Tutorials" class="is-logo-image" loading="eager" width="250" height="80">
					</a>
				</div><form method="get" class="search-form navigation-search" action="https://randomnerdtutorials.com/">
					<input type="search" class="search-field" value="" name="s" title="Search">
				</form>		<div class="mobile-bar-items">
						<span class="search-item">
				<a aria-label="Open Search Bar" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#">
									</a>
			</span>
		</div>
						<button class="menu-toggle" aria-controls="primary-menu" aria-expanded="false">
					<span class="mobile-menu">Menu</span>				</button>
				<div id="primary-menu" class="main-nav"><ul id="menu-newtop" class=" menu sf-menu"><li id="menu-item-20487" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20487"><a href="https://randomnerdtutorials.com/download">Free eBooks</a></li>
<li id="menu-item-20484" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20484"><a href="https://randomnerdtutorials.com/about">About</a></li>
<li id="menu-item-20485" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20485"><a href="https://randomnerdtutorials.com/contact">Contact</a></li>
<li id="menu-item-68854" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-68854"><a target="_blank" rel="noopener" href="https://rntlab.com/login">Courses Login</a></li>
<li id="menu-item-20483" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-has-children menu-item-20483"><a href="https://randomnerdtutorials.com/courses/"><strong>Get Courses</strong><span role="presentation" class="dropdown-menu-toggle"></span></a>
<ul class="sub-menu">
	<li id="menu-item-40154" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40154"><a href="https://randomnerdtutorials.com/courses/"><strong>All eBooks &amp; Courses</strong></a></li>
	<li id="menu-item-100940" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-100940"><a href="https://randomnerdtutorials.com/build-web-servers-esp32-esp8266-ebook/"><strong>Build Web Servers with ESP32 and ESP8266</strong></a></li>
	<li id="menu-item-69105" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-69105"><a href="https://randomnerdtutorials.com/learn-esp32-with-arduino-ide/">Learn ESP32 with Arduino IDE</a></li>
	<li id="menu-item-96038" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-96038"><a href="https://randomnerdtutorials.com/esp32-cam-projects-ebook/">Build ESP32-CAM Projects</a></li>
	<li id="menu-item-83302" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-83302"><a href="https://randomnerdtutorials.com/micropython-programming-with-esp32-and-esp8266/">MicroPython Programming with ESP32 and ESP8266</a></li>
	<li id="menu-item-40149" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40149"><a href="https://randomnerdtutorials.com/home-automation-using-esp8266/">Home Automation Using ESP8266</a></li>
	<li id="menu-item-40150" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40150"><a href="https://randomnerdtutorials.com/build-a-home-automation-system-for-100/">Build a Home Automation System for $100</a></li>
	<li id="menu-item-40151" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40151"><a href="https://randomnerdtutorials.com/arduino-step-by-step-projects/">Arduino Step-by-step Projects</a></li>
	<li id="menu-item-40153" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40153"><a href="https://randomnerdtutorials.com/android-apps-for-arduino-with-mit-app-inventor-2/">Android Apps For Arduino</a></li>
	<li id="menu-item-40152" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-40152"><a href="https://randomnerdtutorials.com/electronics-for-beginners/">Electronics For Beginners</a></li>
</ul>
</li>
<li class="search-item menu-item-align-right"><a aria-label="Open Search Bar" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#"></a></li></ul></div>			</div>
		</nav>
				<header id="masthead" class="site-header" itemtype="https://schema.org/WPHeader" itemscope="">
			<div class="inside-header">
							</div>
		</header>
		
	<div id="page" class="site grid-container container hfeed grid-parent">
		<div style="margin-top:10px; padding:10px;" class="rnt-menu-top-links">
	<a class="rntn-top-menu" href="https://randomnerdtutorials.com/">HOME</a>
  <a class="rntn-top-menu" href="https://randomnerdtutorials.com/projects-esp32/">ESP32</a>
  <a class="rntn-top-menu" href="https://randomnerdtutorials.com/projects-esp8266/">ESP8266</a>
  <a class="rntn-top-menu" href="https://randomnerdtutorials.com/projects-esp32-cam/">ESP32-CAM</a>
  <a class="rntn-top-menu" href="https://randomnerdtutorials.com/projects-esp32-esp8266-micropython/">MICROPYTHON</a>
  <a class="rntn-top-menu" href="https://randomnerdtutorials.com/projects-arduino/">ARDUINO</a>
  <a class="rntn-top-menu" href="https://makeradvisor.com/" target="_blank" rel="noopener">REVIEWS</a>
  <a class="rntn-top-menu" href="https://randomnerdtutorials.com/projects/">PROJECTS</a>
</div>		<div id="content" class="site-content">
			
	<div id="primary" class="content-area grid-parent mobile-grid-100 push-15 grid-60 tablet-push-15 tablet-grid-60">
		<main id="main" class="site-main">
			
<article id="post-67766" class="post-67766 post type-post status-publish format-standard has-post-thumbnail hentry category-esp32 category-esp32-project category-esp32-arduino-ide category-0-esp32 category-project mv-content-wrapper" itemtype="https://schema.org/CreativeWork" itemscope="">
	<div class="inside-article">
					<header class="entry-header">
				<h1 class="entry-title" itemprop="headline">How to Set an ESP32 Access Point (AP) for Web Server</h1>			</header>
			
		<div class="entry-content" itemprop="text">
			
<p>The ESP32 can act as a Wi-Fi station, as an access point, or both. In this tutorial we’ll show you how to set the ESP32 as an access point using Arduino IDE.</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="796" height="448" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/ESP32-access-point-1.jpg" alt="" class="wp-image-67860" srcset="https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg?w=1280&amp;quality=100&amp;strip=all&amp;ssl=1 1280w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg?resize=300%2C169&amp;quality=100&amp;strip=all&amp;ssl=1 300w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg?resize=768%2C432&amp;quality=100&amp;strip=all&amp;ssl=1 768w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point-1.jpg?resize=1024%2C576&amp;quality=100&amp;strip=all&amp;ssl=1 1024w" sizes="(max-width: 828px) 100vw, 828px" loading="eager"></figure></div>



<p>In most projects with the ESP32, we connect the ESP32 to a wireless router (see our <a href="https://randomnerdtutorials.com/esp32-web-server-arduino-ide/">ESP32 web server tutorial</a>). This way we can access the ESP32 through the local network. </p>



<p>In this situation the router acts as an access point and the ESP32 is set as a station. In this scenario, you need to be connected to your router (local network) to control the ESP32.</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="796" height="400" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/esp32-station.png" alt="" class="wp-image-67836" srcset="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-station.png?w=900&amp;quality=100&amp;strip=all&amp;ssl=1 900w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-station.png?resize=300%2C151&amp;quality=100&amp;strip=all&amp;ssl=1 300w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-station.png?resize=768%2C386&amp;quality=100&amp;strip=all&amp;ssl=1 768w" sizes="(max-width: 828px) 100vw, 828px" loading="eager"></figure></div>



<p>But if you set the ESP32 as an access point (hotspot), you can be connected to the ESP32 using any device with Wi-Fi capabilities without the need to connect to your router. </p>



<p>In simple words, when you set the ESP32 as an access point you create its own Wi-Fi network and nearby Wi-Fi devices (stations) can connect to it (like your smartphone or your computer).</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="796" height="468" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/access-point.png" alt="" class="wp-image-67835" srcset="https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/access-point.png?w=800&amp;quality=100&amp;strip=all&amp;ssl=1 800w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/access-point.png?resize=300%2C176&amp;quality=100&amp;strip=all&amp;ssl=1 300w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/access-point.png?resize=768%2C451&amp;quality=100&amp;strip=all&amp;ssl=1 768w" sizes="(max-width: 800px) 100vw, 800px" loading="eager"></figure></div>



<p>Here we’ll show you how to set the ESP32 as an access point in your web server projects. This way, you don’t need to be connected to a router to control your ESP32. Because the ESP32 doesn’t connect further to a wired network (like your router), it is called soft-AP (soft Access Point).</p>



<h2>Installing the ESP32 board in Arduino IDE</h2>



<p>There’s an add-on for the Arduino IDE that allows you to program the ESP32 using the Arduino IDE and its programming language. Follow one of the following tutorials to prepare your Arduino IDE:</p>



<ul><li><a href="https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/"><strong>Windows instructions</strong> – Installing the ESP32 Board in Arduino IDE</a></li><li><a href="https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-mac-and-linux-instructions/"><strong>Mac and Linux instructions</strong> –&nbsp;Installing the ESP32 Board in Arduino IDE</a></li></ul>



<h2>ESP32 Access Point</h2>



<p>In this example, we’ll modify an <a href="https://randomnerdtutorials.com/esp32-web-server-arduino-ide/">ESP32 Web Server</a> from a previous tutorial to add access point capabilities. What we’ll show you here can be used with any ESP32 web server example.</p>



<p>Upload the sketch provided below to set the ESP32 as an access point.</p>


<pre style="max-height: 40em; margin-bottom: 20px;" class=" language-c"><code class=" language-c"><span class="token comment">/*********
  Rui Santos
  Complete project details at https://randomnerdtutorials.com  
*********/</span>

<span class="token comment">// Load Wi-Fi library</span>
<span class="token macro property"><span class="token directive-hash">#</span><span class="token directive keyword">include</span> <span class="token string">&lt;WiFi.h&gt;</span></span>

<span class="token comment">// Replace with your network credentials</span>
<span class="token keyword">const</span> <span class="token keyword">char</span><span class="token operator">*</span> ssid     <span class="token operator">=</span> <span class="token string">"ESP32-Access-Point"</span><span class="token punctuation">;</span>
<span class="token keyword">const</span> <span class="token keyword">char</span><span class="token operator">*</span> password <span class="token operator">=</span> <span class="token string">"123456789"</span><span class="token punctuation">;</span>

<span class="token comment">// Set web server port number to 80</span>
WiFiServer <span class="token function">server</span><span class="token punctuation">(</span><span class="token number">80</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Variable to store the HTTP request</span>
String header<span class="token punctuation">;</span>

<span class="token comment">// Auxiliar variables to store the current output state</span>
String output26State <span class="token operator">=</span> <span class="token string">"off"</span><span class="token punctuation">;</span>
String output27State <span class="token operator">=</span> <span class="token string">"off"</span><span class="token punctuation">;</span>

<span class="token comment">// Assign output variables to GPIO pins</span>
<span class="token keyword">const</span> <span class="token keyword">int</span> output26 <span class="token operator">=</span> <span class="token number">26</span><span class="token punctuation">;</span>
<span class="token keyword">const</span> <span class="token keyword">int</span> output27 <span class="token operator">=</span> <span class="token number">27</span><span class="token punctuation">;</span>

<span class="token keyword">void</span> <span class="token function">setup</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  Serial<span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token number">115200</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token comment">// Initialize the output variables as outputs</span>
  <span class="token function">pinMode</span><span class="token punctuation">(</span>output26<span class="token punctuation">,</span> OUTPUT<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token function">pinMode</span><span class="token punctuation">(</span>output27<span class="token punctuation">,</span> OUTPUT<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token comment">// Set outputs to LOW</span>
  <span class="token function">digitalWrite</span><span class="token punctuation">(</span>output26<span class="token punctuation">,</span> LOW<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token function">digitalWrite</span><span class="token punctuation">(</span>output27<span class="token punctuation">,</span> LOW<span class="token punctuation">)</span><span class="token punctuation">;</span>

  <span class="token comment">// Connect to Wi-Fi network with SSID and password</span>
  Serial<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"Setting AP (Access Point)…"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token comment">// Remove the password parameter, if you want the AP (Access Point) to be open</span>
  WiFi<span class="token punctuation">.</span><span class="token function">softAP</span><span class="token punctuation">(</span>ssid<span class="token punctuation">,</span> password<span class="token punctuation">)</span><span class="token punctuation">;</span>

  IPAddress IP <span class="token operator">=</span> WiFi<span class="token punctuation">.</span><span class="token function">softAPIP</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  Serial<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"AP IP address: "</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  Serial<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span>IP<span class="token punctuation">)</span><span class="token punctuation">;</span>
  
  server<span class="token punctuation">.</span><span class="token function">begin</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token function">loop</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
  WiFiClient client <span class="token operator">=</span> server<span class="token punctuation">.</span><span class="token function">available</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>   <span class="token comment">// Listen for incoming clients</span>

  <span class="token keyword">if</span> <span class="token punctuation">(</span>client<span class="token punctuation">)</span> <span class="token punctuation">{</span>                             <span class="token comment">// If a new client connects,</span>
    Serial<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"New Client."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>          <span class="token comment">// print a message out in the serial port</span>
    String currentLine <span class="token operator">=</span> <span class="token string">""</span><span class="token punctuation">;</span>                <span class="token comment">// make a String to hold incoming data from the client</span>
    <span class="token keyword">while</span> <span class="token punctuation">(</span>client<span class="token punctuation">.</span><span class="token function">connected</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>            <span class="token comment">// loop while the client's connected</span>
      <span class="token keyword">if</span> <span class="token punctuation">(</span>client<span class="token punctuation">.</span><span class="token function">available</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>             <span class="token comment">// if there's bytes to read from the client,</span>
        <span class="token keyword">char</span> c <span class="token operator">=</span> client<span class="token punctuation">.</span><span class="token function">read</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>             <span class="token comment">// read a byte, then</span>
        Serial<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>c<span class="token punctuation">)</span><span class="token punctuation">;</span>                    <span class="token comment">// print it out the serial monitor</span>
        header <span class="token operator">+=</span> c<span class="token punctuation">;</span>
        <span class="token keyword">if</span> <span class="token punctuation">(</span>c <span class="token operator">==</span> <span class="token string">'\n'</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>                    <span class="token comment">// if the byte is a newline character</span>
          <span class="token comment">// if the current line is blank, you got two newline characters in a row.</span>
          <span class="token comment">// that's the end of the client HTTP request, so send a response:</span>
          <span class="token keyword">if</span> <span class="token punctuation">(</span>currentLine<span class="token punctuation">.</span><span class="token function">length</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">==</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// HTTP headers always start with a response code (e.g. HTTP/1.1 200 OK)</span>
            <span class="token comment">// and a content-type so the client knows what's coming, then a blank line:</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"HTTP/1.1 200 OK"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Content-type:text/html"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Connection: close"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// turns the GPIOs on and off</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>header<span class="token punctuation">.</span><span class="token function">indexOf</span><span class="token punctuation">(</span><span class="token string">"GET /26/on"</span><span class="token punctuation">)</span> <span class="token operator">&gt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
              Serial<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"GPIO 26 on"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
              output26State <span class="token operator">=</span> <span class="token string">"on"</span><span class="token punctuation">;</span>
              <span class="token function">digitalWrite</span><span class="token punctuation">(</span>output26<span class="token punctuation">,</span> HIGH<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>header<span class="token punctuation">.</span><span class="token function">indexOf</span><span class="token punctuation">(</span><span class="token string">"GET /26/off"</span><span class="token punctuation">)</span> <span class="token operator">&gt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
              Serial<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"GPIO 26 off"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
              output26State <span class="token operator">=</span> <span class="token string">"off"</span><span class="token punctuation">;</span>
              <span class="token function">digitalWrite</span><span class="token punctuation">(</span>output26<span class="token punctuation">,</span> LOW<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>header<span class="token punctuation">.</span><span class="token function">indexOf</span><span class="token punctuation">(</span><span class="token string">"GET /27/on"</span><span class="token punctuation">)</span> <span class="token operator">&gt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
              Serial<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"GPIO 27 on"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
              output27State <span class="token operator">=</span> <span class="token string">"on"</span><span class="token punctuation">;</span>
              <span class="token function">digitalWrite</span><span class="token punctuation">(</span>output27<span class="token punctuation">,</span> HIGH<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>header<span class="token punctuation">.</span><span class="token function">indexOf</span><span class="token punctuation">(</span><span class="token string">"GET /27/off"</span><span class="token punctuation">)</span> <span class="token operator">&gt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
              Serial<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"GPIO 27 off"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
              output27State <span class="token operator">=</span> <span class="token string">"off"</span><span class="token punctuation">;</span>
              <span class="token function">digitalWrite</span><span class="token punctuation">(</span>output27<span class="token punctuation">,</span> LOW<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            
            <span class="token comment">// Display the HTML web page</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;!DOCTYPE html&gt;&lt;html&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;head&gt;&lt;meta name=\"viewport\" content=\"width=device-width, initial-scale=1\"&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;link rel=\"icon\" href=\"data:,\"&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token comment">// CSS to style the on/off buttons </span>
            <span class="token comment">// Feel free to change the background-color and font-size attributes to fit your preferences</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;style&gt;html { font-family: Helvetica; display: inline-block; margin: 0px auto; text-align: center;}"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">".button { background-color: #4CAF50; border: none; color: white; padding: 16px 40px;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"text-decoration: none; font-size: 30px; margin: 2px; cursor: pointer;}"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">".button2 {background-color: #555555;}&lt;/style&gt;&lt;/head&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Web Page Heading</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;body&gt;&lt;h1&gt;ESP32 Web Server&lt;/h1&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Display current state, and ON/OFF buttons for GPIO 26  </span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt;GPIO 26 - State "</span> <span class="token operator">+</span> output26State <span class="token operator">+</span> <span class="token string">"&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token comment">// If the output26State is off, it displays the ON button       </span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>output26State<span class="token operator">==</span><span class="token string">"off"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
              client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt;&lt;a href=\"/26/on\"&gt;&lt;button class=\"button\"&gt;ON&lt;/button&gt;&lt;/a&gt;&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
              client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt;&lt;a href=\"/26/off\"&gt;&lt;button class=\"button button2\"&gt;OFF&lt;/button&gt;&lt;/a&gt;&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> 
               
            <span class="token comment">// Display current state, and ON/OFF buttons for GPIO 27  </span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt;GPIO 27 - State "</span> <span class="token operator">+</span> output27State <span class="token operator">+</span> <span class="token string">"&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token comment">// If the output27State is off, it displays the ON button       </span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>output27State<span class="token operator">==</span><span class="token string">"off"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
              client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt;&lt;a href=\"/27/on\"&gt;&lt;button class=\"button\"&gt;ON&lt;/button&gt;&lt;/a&gt;&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
              client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt;&lt;a href=\"/27/off\"&gt;&lt;button class=\"button button2\"&gt;OFF&lt;/button&gt;&lt;/a&gt;&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"&lt;/body&gt;&lt;/html&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// The HTTP response ends with another blank line</span>
            client<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token comment">// Break out of the while loop</span>
            <span class="token keyword">break</span><span class="token punctuation">;</span>
          <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span> <span class="token comment">// if you got a newline, then clear currentLine</span>
            currentLine <span class="token operator">=</span> <span class="token string">""</span><span class="token punctuation">;</span>
          <span class="token punctuation">}</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>c <span class="token operator">!=</span> <span class="token string">'\r'</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>  <span class="token comment">// if you got anything else but a carriage return character,</span>
          currentLine <span class="token operator">+=</span> c<span class="token punctuation">;</span>      <span class="token comment">// add it to the end of the currentLine</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
    <span class="token comment">// Clear the header variable</span>
    header <span class="token operator">=</span> <span class="token string">""</span><span class="token punctuation">;</span>
    <span class="token comment">// Close the connection</span>
    client<span class="token punctuation">.</span><span class="token function">stop</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    Serial<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Client disconnected."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    Serial<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
	<p style="text-align:center"><a class="rntwhite" href="https://github.com/RuiSantosdotme/Random-Nerd-Tutorials/raw/master/Projects/ESP32/ESP32_Web_Server_AP.ino" target="_blank">View raw code</a></p>



<h3>Customize the SSID and Password</h3>



<p>You need to define a SSID name and a password to access the ESP32. In this example we’re setting the ESP32 SSID name to <span class="rnthl rntliteral">ESP32-Access-Point</span>, but you can modify the name to whatever you want. The password is <span class="rnthl rntliteral">123456789</span>, but you can also modify it.</p>



<pre class="wp-block-code  language-c"><code class=" language-c"><span class="token comment">// You can customize the SSID name and change the password</span>
<span class="token keyword">const</span> <span class="token keyword">char</span><span class="token operator">*</span> ssid <span class="token operator">=</span> <span class="token string">"ESP32-Access-Point"</span><span class="token punctuation">;</span>
<span class="token keyword">const</span> <span class="token keyword">char</span><span class="token operator">*</span> password <span class="token operator">=</span> <span class="token string">"123456789"</span><span class="token punctuation">;</span></code></pre>



<h3>Setting the ESP32 as an Access Point</h3>



<p>There’s a section in the <span class="rnthl rntliteral">setup()</span> to set the ESP32 as an access point using the <span class="rnthl rntliteral">softAP()</span> method:</p>



<pre class="wp-block-code  language-c"><code class=" language-c">WiFi<span class="token punctuation">.</span><span class="token function">softAP</span><span class="token punctuation">(</span>ssid<span class="token punctuation">,</span> password<span class="token punctuation">)</span><span class="token punctuation">;</span></code></pre>



<p>There are also other optional parameters you can pass to the <span class="rnthl rntliteral">softAP()</span> method. Here’s all the parameters:</p>



<pre class="wp-block-code  language-c"><code class=" language-c"><span class="token punctuation">.</span><span class="token function">softAP</span><span class="token punctuation">(</span><span class="token keyword">const</span> <span class="token keyword">char</span><span class="token operator">*</span> ssid<span class="token punctuation">,</span> <span class="token keyword">const</span> <span class="token keyword">char</span><span class="token operator">*</span> password<span class="token punctuation">,</span> <span class="token keyword">int</span> channel<span class="token punctuation">,</span> <span class="token keyword">int</span> ssid_hidden<span class="token punctuation">,</span> <span class="token keyword">int</span> max_connection<span class="token punctuation">)</span></code></pre>



<ul><li><span class="rnthl rntliteral">SSID</span> (defined earlier): maximum of 63 characters;</li><li><span class="rnthl rntliteral">password</span>(defined earlier): minimum of 8 characters; set to NULL if you want the access point to be open</li><li><span class="rnthl rntliteral">channel</span>: Wi-Fi channel number (1-13)</li><li><span class="rnthl rntliteral">ssid_hidden</span>: (0 = broadcast SSID, 1 = hide SSID)</li><li><span class="rnthl rntliteral">max_connection</span>: maximum simultaneous connected clients (1-4)</li></ul>



<p>Next, we need to get the access point IP address using the <span class="rnthl rntliteral">softAPIP()</span> method and print it in the Serial Monitor.</p>



<pre class="wp-block-code  language-c"><code class=" language-c">IPAddress IP <span class="token operator">=</span> WiFi<span class="token punctuation">.</span><span class="token function">softAPIP</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
Serial<span class="token punctuation">.</span><span class="token function">print</span><span class="token punctuation">(</span><span class="token string">"AP IP address: "</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
Serial<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span>IP<span class="token punctuation">)</span><span class="token punctuation">;</span></code></pre>



<p>These are the snippets of code you need to include in your web server sketches to set the ESP32 as an access point. To learn how the full web server code works, take a look at the <a href="https://randomnerdtutorials.com/esp32-web-server-arduino-ide/">ESP32 Web Server tutorial</a>.</p>



<h2>Parts Required</h2>



<p>For this tutorial you’ll need the following parts:</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="750" height="500" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/esp32-web-server-arduino-ide-parts-required.jpg" alt="" class="wp-image-67768" srcset="https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-web-server-arduino-ide-parts-required.jpg?w=750&amp;quality=100&amp;strip=all&amp;ssl=1 750w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-web-server-arduino-ide-parts-required.jpg?resize=300%2C200&amp;quality=100&amp;strip=all&amp;ssl=1 300w" sizes="(max-width: 750px) 100vw, 750px" loading="eager"></figure></div>



<ul><li><a href="https://makeradvisor.com/tools/esp32-dev-board-wi-fi-bluetooth/" target="_blank" rel="noreferrer noopener">ESP32 development board</a>&nbsp;–&nbsp;&nbsp;<a href="https://makeradvisor.com/esp32-development-boards-review-comparison/" target="_blank" rel="noreferrer noopener">read ESP32 Development Boards Review and Comparison</a></li><li><a href="https://makeradvisor.com/tools/3mm-5mm-leds-kit-storage-box/" target="_blank" rel="noreferrer noopener">2x 5mm LED</a></li><li><a href="https://makeradvisor.com/tools/resistors-kits/" target="_blank" rel="noreferrer noopener">2x 330 Ohm resistor</a></li><li><a href="https://makeradvisor.com/tools/mb-102-solderless-breadboard-830-points/" target="_blank" rel="noreferrer noopener">Breadboard</a></li><li><a href="https://makeradvisor.com/tools/jumper-wires-kit-120-pieces/" target="_blank" rel="noreferrer noopener">Jumper wires</a></li></ul>


<p>You can use the preceding links or go directly to <a href="https://makeradvisor.com/tools/?utm_source=rnt&amp;utm_medium=post&amp;utm_campaign=post" target="_blank">MakerAdvisor.com/tools</a> to find all the parts for your projects at the best price!</p><p style="text-align:center;"><a href="https://makeradvisor.com/tools/?utm_source=rnt&amp;utm_medium=post&amp;utm_campaign=post" target="_blank"><img src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/header-200.png" loading="lazy" width="200" height="56"></a></p>



<h2>Schematic</h2>



<p>Start by building the circuit. Connect two LEDs to the ESP32 as shown in the following schematic diagram – one LED connected to <span class="rnthl rntcblue">GPIO 26</span>, and the other to <span class="rnthl rntcblue">GPIO 27</span>.</p>



<p><strong>Note</strong>: We’re using the ESP32 DEVKIT DOIT board with 36 pins. Before assembling the circuit, make sure you check the pinout for the board you’re using.</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="796" height="566" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/esp32_web_server_schematic.png" alt="" class="wp-image-67732" srcset="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32_web_server_schematic.png?w=984&amp;quality=100&amp;strip=all&amp;ssl=1 984w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32_web_server_schematic.png?resize=300%2C213&amp;quality=100&amp;strip=all&amp;ssl=1 300w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32_web_server_schematic.png?resize=768%2C546&amp;quality=100&amp;strip=all&amp;ssl=1 768w" sizes="(max-width: 828px) 100vw, 828px" loading="lazy"></figure></div>



<h2>ESP32 IP Address</h2>



<p>Upload the code to your ESP32 (make sure you have the right board and COM port selected). Open the Serial Monitor at a baud rate of 115200. Press the ESP32 “Enable” button.</p>



<p>The IP address you need to access the ESP32 point will be printed. In this case, it is <strong>192.168.4.1</strong>.</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="739" height="445" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/ip-address-ap.png" alt="" class="wp-image-67819" srcset="https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ip-address-ap.png?w=739&amp;quality=100&amp;strip=all&amp;ssl=1 739w, https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ip-address-ap.png?resize=300%2C181&amp;quality=100&amp;strip=all&amp;ssl=1 300w" sizes="(max-width: 739px) 100vw, 739px" loading="lazy"></figure></div>



<h2>Connecting to the ESP32 Access Point</h2>



<p>Having the ESP32 running the new sketch, in your smartphone open your Wi-Fi settings and tap the&nbsp;<strong>ESP32-Access-Point&nbsp;</strong>network:</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="600" height="667" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/ESP32-access-point.jpg" alt="" class="wp-image-67822" srcset="https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point.jpg?w=600&amp;quality=100&amp;strip=all&amp;ssl=1 600w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/ESP32-access-point.jpg?resize=270%2C300&amp;quality=100&amp;strip=all&amp;ssl=1 270w" sizes="(max-width: 600px) 100vw, 600px" loading="lazy"></figure></div>



<p>Enter the password you’ve defined earlier in the code.</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="400" height="288" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/access-point-password.jpg" alt="" class="wp-image-67823" srcset="https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/access-point-password.jpg?w=400&amp;quality=100&amp;strip=all&amp;ssl=1 400w, https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/access-point-password.jpg?resize=300%2C216&amp;quality=100&amp;strip=all&amp;ssl=1 300w" sizes="(max-width: 400px) 100vw, 400px" loading="lazy"></figure></div>



<p>Open your web browser and type the IP address 192.168.4.1. The web server page should load:</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="399" height="411" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/esp32-web-server-apoint.jpg" alt="" class="wp-image-67825" srcset="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-web-server-apoint.jpg?w=399&amp;quality=100&amp;strip=all&amp;ssl=1 399w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-web-server-apoint.jpg?resize=291%2C300&amp;quality=100&amp;strip=all&amp;ssl=1 291w" sizes="(max-width: 399px) 100vw, 399px" loading="lazy"></figure></div>



<p>To connect to the access point on your computer, go to the Network and Internet Settings and select the “<strong>ESP32-Access-Point</strong>“.</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="360" height="623" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/esp32-access-point-pc.png" alt="" class="wp-image-67826" srcset="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-access-point-pc.png?w=360&amp;quality=100&amp;strip=all&amp;ssl=1 360w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/esp32-access-point-pc.png?resize=173%2C300&amp;quality=100&amp;strip=all&amp;ssl=1 173w" sizes="(max-width: 360px) 100vw, 360px" loading="lazy"></figure></div>



<p>Insert the password you’ve defined earlier.</p>



<div class="wp-block-image"><figure class="aligncenter"><img width="359" height="620" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/connect-access-point-pc.png" alt="" class="wp-image-67827" srcset="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/connect-access-point-pc.png?w=359&amp;quality=100&amp;strip=all&amp;ssl=1 359w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/07/connect-access-point-pc.png?resize=174%2C300&amp;quality=100&amp;strip=all&amp;ssl=1 174w" sizes="(max-width: 359px) 100vw, 359px" loading="lazy"></figure></div>



<p>And it’s done! Now, to access the ESP32 web server page, you just need to type the ESP32 IP address on your browser.</p>



<h2>Wrapping Up</h2>



<p>This simple tutorial showed you how to set the ESP32 as an access point on your web server sketches. When the ESP32 is set as an access point, devices with Wi-Fi capabilities can connect directly to the ESP32 without the need to connect to a router.</p>



<p>You may also like reading:</p>



<ul><li><a href="https://randomnerdtutorials.com/learn-esp32-with-arduino-ide/"><strong>Learn ESP32 with Arduino IDE (course)</strong></a></li><li><a href="https://randomnerdtutorials.com/esp32-web-server-arduino-ide/">ESP32 Web Server</a></li><li><a href="https://randomnerdtutorials.com/esp32-data-logging-temperature-to-microsd-card/">ESP32 Data Logging Temperature to MicroSD Card</a></li><li><a href="https://randomnerdtutorials.com/esp32-dc-motor-l298n-motor-driver-control-speed-direction/">ESP32 with DC Motor and L298N Motor Driver – Control Speed and Direction</a></li></ul>



<p>We hope you’ve found this tutorial useful.&nbsp;If you like ESP32 and you want to learn more, we recommend enrolling in&nbsp;<a href="https://randomnerdtutorials.com/learn-esp32-with-arduino-ide/"><strong>Learn ESP32 with Arduino IDE</strong>&nbsp;course</a>.</p>



<p>Thanks for reading.</p>
		</div>

		<br>
<center><a href="https://randomnerdtutorials.com/pcbway" target="_blank"><img src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/750x170-updated-f.png" loading="lazy" width="750" height="148"></a></center>
<br>
		<div data-elementor-type="section" data-elementor-id="83032" class="elementor elementor-83032" data-elementor-settings="[]">
		<div class="elementor-section-wrap">
					<section class="elementor-section elementor-top-section elementor-element elementor-element-2d8a9105 elementor-section-boxed elementor-section-height-default elementor-section-height-default" data-id="2d8a9105" data-element_type="section">
						<div class="elementor-container elementor-column-gap-default">
							<div class="elementor-row">
					<div class="elementor-column elementor-col-100 elementor-top-column elementor-element elementor-element-2280806f" data-id="2280806f" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<section class="elementor-section elementor-inner-section elementor-element elementor-element-4a840dd4 elementor-section-boxed elementor-section-height-default elementor-section-height-default" data-id="4a840dd4" data-element_type="section">
						<div class="elementor-container elementor-column-gap-default">
							<div class="elementor-row">
					<div class="elementor-column elementor-col-50 elementor-inner-column elementor-element elementor-element-3497580" data-id="3497580" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<div class="elementor-element elementor-element-7b0162e9 elementor-widget elementor-widget-image" data-id="7b0162e9" data-element_type="widget" data-widget_type="image.default">
				<div class="elementor-widget-container">
								<div class="elementor-image">
													<a href="https://randomnerdtutorials.com/build-web-servers-esp32-esp8266-ebook/">
							<img src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/Build-Web-Servers-with-ESP32-and-ESP8266-eBook-2nd-Edition-500px-h-p2lw6wwnkk9ystvwe9iof8zx6yt4x7uma3cqfup534.jpg" title="Build-Web-Servers-with-ESP32-and-ESP8266-eBook-2nd-Edition-500px-h" alt="Build-Web-Servers-with-ESP32-and-ESP8266-eBook-2nd-Edition-500px-h" loading="lazy" width="129" height="180">								</a>
														</div>
						</div>
				</div>
						</div>
					</div>
		</div>
				<div class="elementor-column elementor-col-50 elementor-inner-column elementor-element elementor-element-45a69540" data-id="45a69540" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<div class="elementor-element elementor-element-d7f411a elementor-widget elementor-widget-heading" data-id="d7f411a" data-element_type="widget" data-widget_type="heading.default">
				<div class="elementor-widget-container">
			<h4 class="elementor-heading-title elementor-size-default"><a href="https://randomnerdtutorials.com/build-web-servers-esp32-esp8266-ebook/">[eBook] Build Web Servers with ESP32 and ESP8266 (2nd Edition)</a></h4>		</div>
				</div>
				<div class="elementor-element elementor-element-5dc4402f elementor-hidden-phone elementor-widget elementor-widget-text-editor" data-id="5dc4402f" data-element_type="widget" data-widget_type="text-editor.default">
				<div class="elementor-widget-container">
								<div class="elementor-text-editor elementor-clearfix">
					Build Web Server projects with the ESP32 and ESP8266 boards to control outputs and monitor sensors remotely. Learn HTML, CSS, JavaScript and client-server communication protocols&nbsp;<strong><a href="https://randomnerdtutorials.com/build-web-servers-esp32-esp8266-ebook/" rel="noopener">DOWNLOAD »</a></strong>					</div>
						</div>
				</div>
						</div>
					</div>
		</div>
								</div>
					</div>
		</section>
				<div class="elementor-element elementor-element-4de314b8 elementor-hidden-desktop elementor-hidden-tablet elementor-widget elementor-widget-text-editor" data-id="4de314b8" data-element_type="widget" data-widget_type="text-editor.default">
				<div class="elementor-widget-container">
								<div class="elementor-text-editor elementor-clearfix">
					<p>Build Web Server projects with the ESP32 and ESP8266 boards to control outputs and monitor sensors remotely. Learn HTML, CSS, JavaScript and client-server communication protocols&nbsp;<strong><a href="https://randomnerdtutorials.com/build-web-servers-esp32-esp8266-ebook/" rel="noopener">DOWNLOAD »</a></strong></p>					</div>
						</div>
				</div>
						</div>
					</div>
		</div>
								</div>
					</div>
		</section>
				</div>
		</div>
		
		<div data-elementor-type="section" data-elementor-id="82533" class="elementor elementor-82533" data-elementor-settings="[]">
		<div class="elementor-section-wrap">
					<section class="elementor-section elementor-top-section elementor-element elementor-element-31c9920 elementor-section-boxed elementor-section-height-default elementor-section-height-default" data-id="31c9920" data-element_type="section">
						<div class="elementor-container elementor-column-gap-default">
							<div class="elementor-row">
					<div class="elementor-column elementor-col-100 elementor-top-column elementor-element elementor-element-e6bec81" data-id="e6bec81" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<div class="elementor-element elementor-element-ae5f36f elementor-widget elementor-widget-text-editor" data-id="ae5f36f" data-element_type="widget" data-widget_type="text-editor.default">
				<div class="elementor-widget-container">
								<div class="elementor-text-editor elementor-clearfix">
					<h3>Recommended Resources</h3>					</div>
						</div>
				</div>
						</div>
					</div>
		</div>
								</div>
					</div>
		</section>
				<section class="elementor-section elementor-top-section elementor-element elementor-element-df31b19 elementor-section-boxed elementor-section-height-default elementor-section-height-default" data-id="df31b19" data-element_type="section">
						<div class="elementor-container elementor-column-gap-default">
							<div class="elementor-row">
					<div class="elementor-column elementor-col-33 elementor-top-column elementor-element elementor-element-f988f78" data-id="f988f78" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<div class="elementor-element elementor-element-ea4ffd5 elementor-widget elementor-widget-image" data-id="ea4ffd5" data-element_type="widget" data-widget_type="image.default">
				<div class="elementor-widget-container">
								<div class="elementor-image">
													<a href="https://randomnerdtutorials.com/build-a-home-automation-system-for-100/">
							<img width="400" height="225" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/home-automation-sb-img.jpg" class="attachment-full size-full" alt="" srcset="https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2017/10/home-automation-sb-img.jpg?w=400&amp;quality=100&amp;strip=all&amp;ssl=1 400w, https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2017/10/home-automation-sb-img.jpg?resize=300%2C169&amp;quality=100&amp;strip=all&amp;ssl=1 300w" sizes="(max-width: 400px) 100vw, 400px" loading="lazy">								</a>
														</div>
						</div>
				</div>
				<div class="elementor-element elementor-element-1d03956 elementor-widget elementor-widget-text-editor" data-id="1d03956" data-element_type="widget" data-widget_type="text-editor.default">
				<div class="elementor-widget-container">
								<div class="elementor-text-editor elementor-clearfix">
					<p><strong><a href="https://randomnerdtutorials.com/build-a-home-automation-system-for-100/">Build a Home Automation System from Scratch »</a>&nbsp;</strong>With Raspberry Pi, ESP8266, Arduino, and Node-RED.</p>					</div>
						</div>
				</div>
						</div>
					</div>
		</div>
				<div class="elementor-column elementor-col-33 elementor-top-column elementor-element elementor-element-c804b9b" data-id="c804b9b" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<div class="elementor-element elementor-element-caff517 elementor-widget elementor-widget-image" data-id="caff517" data-element_type="widget" data-widget_type="image.default">
				<div class="elementor-widget-container">
								<div class="elementor-image">
													<a href="https://randomnerdtutorials.com/home-automation-using-esp8266/">
							<img width="400" height="225" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/esp8266-sb-img.jpg" class="attachment-full size-full" alt="" srcset="https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2017/10/esp8266-sb-img.jpg?w=400&amp;quality=100&amp;strip=all&amp;ssl=1 400w, https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2017/10/esp8266-sb-img.jpg?resize=300%2C169&amp;quality=100&amp;strip=all&amp;ssl=1 300w" sizes="(max-width: 400px) 100vw, 400px" loading="lazy">								</a>
														</div>
						</div>
				</div>
				<div class="elementor-element elementor-element-7bc712f elementor-widget elementor-widget-text-editor" data-id="7bc712f" data-element_type="widget" data-widget_type="text-editor.default">
				<div class="elementor-widget-container">
								<div class="elementor-text-editor elementor-clearfix">
					<p><strong><a href="https://randomnerdtutorials.com/home-automation-using-esp8266/">Home Automation using ESP8266 eBook and video course »</a>&nbsp;</strong>Build IoT and home automation projects.</p>					</div>
						</div>
				</div>
						</div>
					</div>
		</div>
				<div class="elementor-column elementor-col-33 elementor-top-column elementor-element elementor-element-9487535" data-id="9487535" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<div class="elementor-element elementor-element-330785f elementor-widget elementor-widget-image" data-id="330785f" data-element_type="widget" data-widget_type="image.default">
				<div class="elementor-widget-container">
								<div class="elementor-image">
													<a href="https://randomnerdtutorials.com/arduino-step-by-step-projects/">
							<img width="400" height="225" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/arduino-sb-img.jpg" class="attachment-full size-full" alt="" srcset="https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2017/10/arduino-sb-img.jpg?w=400&amp;quality=100&amp;strip=all&amp;ssl=1 400w, https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2017/10/arduino-sb-img.jpg?resize=300%2C169&amp;quality=100&amp;strip=all&amp;ssl=1 300w" sizes="(max-width: 400px) 100vw, 400px" loading="lazy">								</a>
														</div>
						</div>
				</div>
				<div class="elementor-element elementor-element-e9540a9 elementor-widget elementor-widget-text-editor" data-id="e9540a9" data-element_type="widget" data-widget_type="text-editor.default">
				<div class="elementor-widget-container">
								<div class="elementor-text-editor elementor-clearfix">
					<p><strong><a href="https://randomnerdtutorials.com/arduino-step-by-step-projects/">Arduino Step-by-Step Projects »</a> </strong>Build 25 Arduino projects with our course, even with no prior experience!</p>					</div>
						</div>
				</div>
						</div>
					</div>
		</div>
								</div>
					</div>
		</section>
				<section class="elementor-section elementor-top-section elementor-element elementor-element-a9e9c13 elementor-section-boxed elementor-section-height-default elementor-section-height-default" data-id="a9e9c13" data-element_type="section">
						<div class="elementor-container elementor-column-gap-default">
							<div class="elementor-row">
					<div class="elementor-column elementor-col-100 elementor-top-column elementor-element elementor-element-25cf7ca" data-id="25cf7ca" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<div class="elementor-element elementor-element-88fc6c0 elementor-widget elementor-widget-text-editor" data-id="88fc6c0" data-element_type="widget" data-widget_type="text-editor.default">
				<div class="elementor-widget-container">
								<div class="elementor-text-editor elementor-clearfix">
					<h3>What to Read Next…</h3>					</div>
						</div>
				</div>
						</div>
					</div>
		</div>
								</div>
					</div>
		</section>
				<section class="elementor-section elementor-top-section elementor-element elementor-element-d68ef93 elementor-section-height-min-height elementor-section-boxed elementor-section-height-default elementor-section-items-middle" data-id="d68ef93" data-element_type="section">
						<div class="elementor-container elementor-column-gap-no">
							<div class="elementor-row">
					<div class="elementor-column elementor-col-100 elementor-top-column elementor-element elementor-element-4ab337a" data-id="4ab337a" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<div class="elementor-element elementor-element-efac60e elementor-grid-3 elementor-grid-tablet-2 elementor-grid-mobile-1 elementor-posts--thumbnail-top elementor-card-shadow-yes elementor-posts__hover-gradient elementor-widget elementor-widget-posts" data-id="efac60e" data-element_type="widget" data-settings="{&quot;cards_row_gap&quot;:{&quot;unit&quot;:&quot;px&quot;,&quot;size&quot;:16,&quot;sizes&quot;:[]},&quot;cards_columns&quot;:&quot;3&quot;,&quot;cards_columns_tablet&quot;:&quot;2&quot;,&quot;cards_columns_mobile&quot;:&quot;1&quot;}" data-widget_type="posts.cards">
				<div class="elementor-widget-container">
					<div class="elementor-posts-container elementor-posts elementor-posts--skin-cards elementor-grid elementor-has-item-ratio">
				<article class="elementor-post elementor-grid-item post-81978 post type-post status-publish format-standard has-post-thumbnail hentry category-esp32 category-esp32-project category-esp8266-project category-0-esp32-micropython category-project mv-content-wrapper">
			<div class="elementor-post__card">
				<a class="elementor-post__thumbnail__link" href="https://randomnerdtutorials.com/micropython-interrupts-esp32-esp8266/">
			<div class="elementor-post__thumbnail"><img width="1280" height="720" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/interrupts-micropython-esp32-esp8266.jpg" class="attachment-full size-full" alt="" srcset="https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2019/03/interrupts-micropython-esp32-esp8266.jpg?w=1280&amp;quality=100&amp;strip=all&amp;ssl=1 1280w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2019/03/interrupts-micropython-esp32-esp8266.jpg?resize=300%2C169&amp;quality=100&amp;strip=all&amp;ssl=1 300w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2019/03/interrupts-micropython-esp32-esp8266.jpg?resize=768%2C432&amp;quality=100&amp;strip=all&amp;ssl=1 768w, https://i2.wp.com/randomnerdtutorials.com/wp-content/uploads/2019/03/interrupts-micropython-esp32-esp8266.jpg?resize=1024%2C576&amp;quality=100&amp;strip=all&amp;ssl=1 1024w" sizes="(max-width: 1280px) 100vw, 1280px" loading="lazy"></div>
		</a>
				<div class="elementor-post__text">
				<h3 class="elementor-post__title">
			<a href="https://randomnerdtutorials.com/micropython-interrupts-esp32-esp8266/">
				MicroPython: Interrupts with ESP32 and ESP8266			</a>
		</h3>
				</div>
					</div>
		</article>
				<article class="elementor-post elementor-grid-item post-12260 post type-post status-publish format-standard has-post-thumbnail hentry category-arduino category-arduino-ide category-esp8266 category-esp8266-project category-esp8266-arduino-ide category-esp8266-projects category-0-esp8266 category-project category-web-server mv-content-wrapper">
			<div class="elementor-post__card">
				<a class="elementor-post__thumbnail__link" href="https://randomnerdtutorials.com/esp8266-remote-controlled-sockets/">
			<div class="elementor-post__thumbnail elementor-fit-height"><img width="700" height="392" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/thumbnail-remote-controlled-sockets-700.jpg" class="attachment-full size-full" alt="" srcset="https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2015/09/thumbnail-remote-controlled-sockets-700.jpg?w=700&amp;quality=100&amp;strip=all&amp;ssl=1 700w, https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2015/09/thumbnail-remote-controlled-sockets-700.jpg?resize=300%2C168&amp;quality=100&amp;strip=all&amp;ssl=1 300w" sizes="(max-width: 700px) 100vw, 700px" loading="lazy"></div>
		</a>
				<div class="elementor-post__text">
				<h3 class="elementor-post__title">
			<a href="https://randomnerdtutorials.com/esp8266-remote-controlled-sockets/">
				ESP8266 Remote Controlled Sockets			</a>
		</h3>
				</div>
					</div>
		</article>
				<article class="elementor-post elementor-grid-item post-92152 post type-post status-publish format-standard has-post-thumbnail hentry category-esp32 category-esp32-project category-esp32-arduino-ide category-0-esp32 category-project mv-content-wrapper">
			<div class="elementor-post__card">
				<a class="elementor-post__thumbnail__link" href="https://randomnerdtutorials.com/esp32-client-server-wi-fi/">
			<div class="elementor-post__thumbnail"><img width="1280" height="720" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/ESP32-Client-Server-Wi-Fi-Communication-Between-Two-Boards.jpg" class="attachment-full size-full" alt="ESP32 Client-Server Wi-Fi Communication Between Two Boards" srcset="https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2020/01/ESP32-Client-Server-Wi-Fi-Communication-Between-Two-Boards.jpg?w=1280&amp;quality=100&amp;strip=all&amp;ssl=1 1280w, https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2020/01/ESP32-Client-Server-Wi-Fi-Communication-Between-Two-Boards.jpg?resize=300%2C169&amp;quality=100&amp;strip=all&amp;ssl=1 300w, https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2020/01/ESP32-Client-Server-Wi-Fi-Communication-Between-Two-Boards.jpg?resize=1024%2C576&amp;quality=100&amp;strip=all&amp;ssl=1 1024w, https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2020/01/ESP32-Client-Server-Wi-Fi-Communication-Between-Two-Boards.jpg?resize=768%2C432&amp;quality=100&amp;strip=all&amp;ssl=1 768w" sizes="(max-width: 1280px) 100vw, 1280px" loading="lazy"></div>
		</a>
				<div class="elementor-post__text">
				<h3 class="elementor-post__title">
			<a href="https://randomnerdtutorials.com/esp32-client-server-wi-fi/">
				ESP32 Client-Server Wi-Fi Communication Between Two Boards			</a>
		</h3>
				</div>
					</div>
		</article>
				</div>
				</div>
				</div>
						</div>
					</div>
		</div>
								</div>
					</div>
		</section>
				</div>
		</div>
		
<br>
		<div data-elementor-type="section" data-elementor-id="82829" class="elementor elementor-82829" data-elementor-settings="[]">
		<div class="elementor-section-wrap">
					<section class="elementor-section elementor-top-section elementor-element elementor-element-1e028b5e elementor-section-boxed elementor-section-height-default elementor-section-height-default" data-id="1e028b5e" data-element_type="section">
						<div class="elementor-container elementor-column-gap-default">
							<div class="elementor-row">
					<div class="elementor-column elementor-col-100 elementor-top-column elementor-element elementor-element-69628243" data-id="69628243" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<section class="elementor-section elementor-inner-section elementor-element elementor-element-4a02bbce elementor-section-boxed elementor-section-height-default elementor-section-height-default" data-id="4a02bbce" data-element_type="section">
						<div class="elementor-container elementor-column-gap-default">
							<div class="elementor-row">
					<div class="elementor-column elementor-col-100 elementor-inner-column elementor-element elementor-element-3a76ce22" data-id="3a76ce22" data-element_type="column">
			<div class="elementor-column-wrap elementor-element-populated">
							<div class="elementor-widget-wrap">
						<div class="elementor-element elementor-element-d86fe9d elementor-widget elementor-widget-heading" data-id="d86fe9d" data-element_type="widget" data-widget_type="heading.default">
				<div class="elementor-widget-container">
			<h3 class="elementor-heading-title elementor-size-default">Enjoyed this project? Stay updated by subscribing our newsletter!</h3>		</div>
				</div>
				<div class="elementor-element elementor-element-93ef837 elementor-button-align-stretch elementor-widget elementor-widget-form" data-id="93ef837" data-element_type="widget" data-settings="{&quot;button_width&quot;:&quot;33&quot;,&quot;step_next_label&quot;:&quot;Next&quot;,&quot;step_previous_label&quot;:&quot;Previous&quot;,&quot;step_type&quot;:&quot;number_text&quot;,&quot;step_icon_shape&quot;:&quot;circle&quot;}" data-widget_type="form.default">
				<div class="elementor-widget-container">
					<form class="elementor-form" method="post" name="New Form">
			<input type="hidden" name="post_id" value="82829">
			<input type="hidden" name="form_id" value="93ef837">
			<input type="hidden" name="referer_title" value="ESP32 Access Point (AP) for Web Server | Random Nerd Tutorials">

							<input type="hidden" name="queried_id" value="67766">
			
			<div class="elementor-form-fields-wrapper elementor-labels-">
								<div class="elementor-field-type-email elementor-field-group elementor-column elementor-field-group-email elementor-col-66 elementor-field-required">
					<label for="form-field-email" class="elementor-field-label elementor-screen-only">Email</label><input size="1" type="email" name="form_fields[email]" id="form-field-email" class="elementor-field elementor-size-sm  elementor-field-textual" placeholder="Your Email Address" required="required" aria-required="true">				</div>
								<div class="elementor-field-group elementor-column elementor-field-type-submit elementor-col-33 e-form__buttons">
					<button type="submit" class="elementor-button elementor-size-sm">
						<span>
															<span class=" elementor-button-icon">
																										</span>
																						<span class="elementor-button-text">SUBSCRIBE</span>
													</span>
					</button>
				</div>
			</div>
		</form>
				</div>
				</div>
						</div>
					</div>
		</div>
								</div>
					</div>
		</section>
						</div>
					</div>
		</div>
								</div>
					</div>
		</section>
				</div>
		</div>
			</div>
</article>

			<div class="comments-area">
				<div id="comments" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">

	<h3 class="comments-title">94 thoughts on “How to Set an ESP32 Access Point (AP) for Web Server”</h3>
		<ol class="comment-list">
			
		<li id="comment-330015" class="comment even thread-even depth-1 parent">
			<article id="div-comment-330015" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/120e8fd877316c3c34efdf7db4251951.png" srcset="https://secure.gravatar.com/avatar/120e8fd877316c3c34efdf7db4251951?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Gabriel</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-330015">
								<time datetime="2018-08-09T18:48:18+00:00" itemprop="datePublished">
									August 9, 2018 at 6:48 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Sara hi Rui,<br>
Thank you very much for your last posts about esp32.<br>
I’m a bit lost in “Wifi libraries”.<br>
My question : For Arduino, Esp8266 or ESP32, is it the same wifi.h library ?<br>
I tried to find an answer in you different posts but it seems not to be precisely indicated.<br>
Best regards</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=330015#respond" data-commentid="330015" data-postid="67766" data-belowelement="div-comment-330015" data-respondelement="respond" data-replyto="Reply to Gabriel" aria-label="Reply to Gabriel">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-330135" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2">
			<article id="div-comment-330135" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-330135">
								<time datetime="2018-08-12T10:41:40+00:00" itemprop="datePublished">
									August 12, 2018 at 10:41 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Gabriel.<br>
With the ESP32 and Arduino we use the WiFi.h library. However, those libraries are different for the ESP32 and ESP8266. If you’re having trouble compiling ESP32 code that uses the WiFi.h library, you must remove the Arduino WiFi library from your Arduino IDE installation.<br>
The ESP8266 uses the ESP8266WiFi.h library.<br>
Regards,<br>
Sara <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=330135#respond" data-commentid="330135" data-postid="67766" data-belowelement="div-comment-330135" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-330030" class="comment even thread-odd thread-alt depth-1 parent">
			<article id="div-comment-330030" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1164a1214160fa30b9a7cabb352ae0aa.jpeg" srcset="https://secure.gravatar.com/avatar/1164a1214160fa30b9a7cabb352ae0aa?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Duncan Amos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-330030">
								<time datetime="2018-08-09T20:25:35+00:00" itemprop="datePublished">
									August 9, 2018 at 8:25 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>It’s the “max_connection” limitation of. “1-4” that puts this outside the range of being really useful.</p>
<p>The Raspberry Pi will get to about 30 and then begin throttling back.</p>
<p>For just a home Website, it might be useful, I suppose.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=330030#respond" data-commentid="330030" data-postid="67766" data-belowelement="div-comment-330030" data-respondelement="respond" data-replyto="Reply to Duncan Amos" aria-label="Reply to Duncan Amos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-565499" class="comment odd alt depth-2">
			<article id="div-comment-565499" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/9785ee8e0c048190289315882507c591.png" srcset="https://secure.gravatar.com/avatar/9785ee8e0c048190289315882507c591?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Tom Olsen</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-565499">
								<time datetime="2021-03-03T15:09:00+00:00" itemprop="datePublished">
									March 3, 2021 at 3:09 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>The primary purpose of this code is to connect to the ESP32 device to configure its internal settings. Not to run a website on.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=565499#respond" data-commentid="565499" data-postid="67766" data-belowelement="div-comment-565499" data-respondelement="respond" data-replyto="Reply to Tom Olsen" aria-label="Reply to Tom Olsen">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-330039" class="comment even thread-even depth-1">
			<article id="div-comment-330039" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/5d780b1ab3951c4a5397703112516b8b.png" srcset="https://secure.gravatar.com/avatar/5d780b1ab3951c4a5397703112516b8b?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn"><a href="http://kain%20construction.com/" rel="external nofollow ugc" class="url">Kevin Kain</a></cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-330039">
								<time datetime="2018-08-09T22:34:31+00:00" itemprop="datePublished">
									August 9, 2018 at 10:34 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Very Nice work. I love this post ! I am trying to do something similar with JSON to read sensors and control pins.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=330039#respond" data-commentid="330039" data-postid="67766" data-belowelement="div-comment-330039" data-respondelement="respond" data-replyto="Reply to Kevin Kain" aria-label="Reply to Kevin Kain">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-332554" class="comment odd alt thread-odd thread-alt depth-1 parent">
			<article id="div-comment-332554" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e93d419ef9c70be1e45141aeb6898bf6.png" srcset="https://secure.gravatar.com/avatar/e93d419ef9c70be1e45141aeb6898bf6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Michele</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332554">
								<time datetime="2018-08-26T22:03:06+00:00" itemprop="datePublished">
									August 26, 2018 at 10:03 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Ciao, e complimenti per l’articolo che trovo particolarmente interessante.<br>
Ho modificato il codice adattandolo a una scheda diversa, e più precisamente NodeMcu Lolin V.3, ma quando cerco di caricare il codice mi dà questo errore. Mi aiuteresti a capire il problema?</p>
<p>Hello, and congratulations for the article that I find particularly interesting.<br>
I modified the code by adapting it to a different card, and more specifically NodeMcu Lolin V.3, but when I try to load the code it gives me this error. Would you help me to understand the problem?</p>
<p>C:\Users\miche\Documents\Arduino\Rui_Santos_AP_Server_Modificato\Rui_Santos_AP_Server_Modificato.ino: In function ‘void setup()’:</p>
<p>Rui_Santos_AP_Server_Modificato:44: error: ‘class WiFiClass’ has no member named ‘softAP’</p>
<p>   WiFi.softAP(ssid, password);</p>
<p>        ^</p>
<p>Rui_Santos_AP_Server_Modificato:46: error: ‘class WiFiClass’ has no member named ‘softAP’</p>
<p>   IPAddress IP = WiFi.softAP();</p>
<p>                       ^</p>
<p>Uso la libreria WiFi alla versione 1.2.7 nella cartella: C:\Program Files\WindowsApps\ArduinoLLC.ArduinoIDE_1.8.10.0_x86__mdqgnx93n4wtt\libraries\WiFi<br>
Uso la libreria SPI alla versione 1.0 nella cartella: C:\Users\miche\Documents\ArduinoData\packages\esp8266\hardware\esp8266\2.4.0\libraries\SPI<br>
exit status 1<br>
‘class WiFiClass’ has no member named ‘softAP’</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=332554#respond" data-commentid="332554" data-postid="67766" data-belowelement="div-comment-332554" data-respondelement="respond" data-replyto="Reply to Michele" aria-label="Reply to Michele">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-332593" class="comment byuser comment-author-sara-santos bypostauthor even depth-2 parent">
			<article id="div-comment-332593" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332593">
								<time datetime="2018-08-27T14:58:32+00:00" itemprop="datePublished">
									August 27, 2018 at 2:58 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
I think you’re not using the right WiFi library. It seems your code is using the ESP8266 wifi library instead of the ESP32.<br>
Also, make sure you’re selecting the right board when you’re trying to upload code.<br>
Can you re-install the ESP32 add-on on your Arduino IDE?<br>
<a href="https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/" rel="nofollow ugc">https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/</a><br>
Also, make sure you have the latest version of the Arduino IDE.<br>
I hope this helps.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=332593#respond" data-commentid="332593" data-postid="67766" data-belowelement="div-comment-332593" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-332624" class="comment odd alt depth-3 parent">
			<article id="div-comment-332624" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e93d419ef9c70be1e45141aeb6898bf6.png" srcset="https://secure.gravatar.com/avatar/e93d419ef9c70be1e45141aeb6898bf6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Michele</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332624">
								<time datetime="2018-08-28T05:02:37+00:00" itemprop="datePublished">
									August 28, 2018 at 5:02 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Ciao, e grazie per la risposta.<br>
Ieri ho aggiornato il mio IDE e installato il componente aggiuntivo ESP32, ma sembra di capire che le librerie vengono richiamate automaticamente dal codice in base alla scheda selezionata, e la mia scheda non è un ESP32 ma una NodeMcu (8266, giusto?) forse il problema è la scheda. Lo sketch è ottimizzato per ESP32 ma la mia scheda non lo è. Chiedo se altri hanno avuto il mio stesso problema, e se lo hanno risolto, magari modificando il codice.</p>
<p>Hello and thanks for the reply. Yesterday I updated my IDE and installed the ESP32 add-on, but it seems to understand that the libraries are automatically recalled by the code according to the selected card, and my card is not an ESP32 but a NodeMcu (8266, right?) Maybe the problem is the card. The sketch is optimized for ESP32 but my card is not. I ask if others have had the same problem, and if they have solved it, maybe by changing the code.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=332624#respond" data-commentid="332624" data-postid="67766" data-belowelement="div-comment-332624" data-respondelement="respond" data-replyto="Reply to Michele" aria-label="Reply to Michele">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-332653" class="comment byuser comment-author-sara-santos bypostauthor even depth-4 parent">
			<article id="div-comment-332653" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332653">
								<time datetime="2018-08-28T13:48:14+00:00" itemprop="datePublished">
									August 28, 2018 at 1:48 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi again.<br>
Sorry. But I didn’t understand: are you using an ESP8266 or an ESP32?</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=332653#respond" data-commentid="332653" data-postid="67766" data-belowelement="div-comment-332653" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-332681" class="comment odd alt depth-5 parent">
			<article id="div-comment-332681" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e93d419ef9c70be1e45141aeb6898bf6.png" srcset="https://secure.gravatar.com/avatar/e93d419ef9c70be1e45141aeb6898bf6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Michele</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332681">
								<time datetime="2018-08-29T05:12:59+00:00" itemprop="datePublished">
									August 29, 2018 at 5:12 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Ciao Sara, io uso questa scheda: <a href="https://www.aliexpress.com/item/-/32648996273.html" rel="nofollow ugc">https://www.aliexpress.com/item/-/32648996273.html</a></p>
				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-332746" class="comment byuser comment-author-sara-santos bypostauthor even depth-5">
			<article id="div-comment-332746" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332746">
								<time datetime="2018-08-29T09:00:32+00:00" itemprop="datePublished">
									August 29, 2018 at 9:00 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi again.<br>
You’re using an ESP8266. The code in this example is for the ESP32, that’s why it doesn’t work.<br>
Try taking a look at this tutorial that shows how to set an access point for the ESP8266:<br>
github.com/esp8266/Arduino/blob/master/doc/esp8266wifi/soft-access-point-examples.rst<br>
I hope this helps.<br>
Regards,<br>
Sara <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"></p>
				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-332755" class="comment odd alt thread-even depth-1 parent">
			<article id="div-comment-332755" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e93d419ef9c70be1e45141aeb6898bf6.png" srcset="https://secure.gravatar.com/avatar/e93d419ef9c70be1e45141aeb6898bf6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Michele</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332755">
								<time datetime="2018-08-29T11:30:24+00:00" itemprop="datePublished">
									August 29, 2018 at 11:30 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Ciao Sara, grazie infinite. È come temevo, il codice qui descritto non va bene per la mia scheda.<br>
Appena posso uso il codice da te indicato e ti faccio sapere.<br>
Grazie ancora, a presto.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=332755#respond" data-commentid="332755" data-postid="67766" data-belowelement="div-comment-332755" data-respondelement="respond" data-replyto="Reply to Michele" aria-label="Reply to Michele">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-332768" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-332768" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332768">
								<time datetime="2018-08-29T15:20:33+00:00" itemprop="datePublished">
									August 29, 2018 at 3:20 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Good luck with your project! I hope you make it work.<br>
P.S. Next time, try to post your questions in english, so that everyone is able to understand.<br>
Thanks.<br>
Regards,<br>
Sara <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=332768#respond" data-commentid="332768" data-postid="67766" data-belowelement="div-comment-332768" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-332784" class="comment odd alt thread-odd thread-alt depth-1 parent">
			<article id="div-comment-332784" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e93d419ef9c70be1e45141aeb6898bf6.png" srcset="https://secure.gravatar.com/avatar/e93d419ef9c70be1e45141aeb6898bf6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Michele</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332784">
								<time datetime="2018-08-29T20:05:52+00:00" itemprop="datePublished">
									August 29, 2018 at 8:05 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hello Sara, I just wanted to apologize to you and everyone in the forum for posting my last questions in my mother tongue rather than in English. Unfortunately for my distraction I did not think to do the translation before publishing them.<br>
I hope I did not create inconvenience to those who followed these posts.<br>
Thank you again for your availability, I offer my regards.<br>
Michele</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=332784#respond" data-commentid="332784" data-postid="67766" data-belowelement="div-comment-332784" data-respondelement="respond" data-replyto="Reply to Michele" aria-label="Reply to Michele">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-332811" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-332811" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-332811">
								<time datetime="2018-08-30T09:08:14+00:00" itemprop="datePublished">
									August 30, 2018 at 9:08 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>You don’t need to worry about that!<br>
Thank you!<br>
Regards,<br>
Sara <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=332811#respond" data-commentid="332811" data-postid="67766" data-belowelement="div-comment-332811" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-340105" class="comment odd alt thread-even depth-1 parent">
			<article id="div-comment-340105" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/6fd95c0c59259b542f00cf08f41c2b42.png" srcset="https://secure.gravatar.com/avatar/6fd95c0c59259b542f00cf08f41c2b42?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Virapong</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-340105">
								<time datetime="2018-10-21T04:22:28+00:00" itemprop="datePublished">
									October 21, 2018 at 4:22 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>i would like to Set an ESP32 Access Point (AP) with static/fix IP address, what i have to modify in Arduio sketch code.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=340105#respond" data-commentid="340105" data-postid="67766" data-belowelement="div-comment-340105" data-respondelement="respond" data-replyto="Reply to Virapong" aria-label="Reply to Virapong">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-340185" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-340185" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-340185">
								<time datetime="2018-10-21T15:53:13+00:00" itemprop="datePublished">
									October 21, 2018 at 3:53 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
You have to insert the following lines in your code to give your ESP32 network a name, and a password. It can be whatever you want.<br>
const char* ssid     = “ESP32-Access-Point”;<br>
const char* password = “123456789”;<br>
Then, set the access point with the following line:<br>
WiFi.softAP(ssid, password);<br>
And get the IP address with the following:<br>
IPAddress IP = WiFi.softAPIP();<br>
Serial.print(“AP IP address: “);<br>
Serial.println(IP);<br>
Everything is explained in the tutorial.<br>
Regards,<br>
Sara <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=340185#respond" data-commentid="340185" data-postid="67766" data-belowelement="div-comment-340185" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-643102" class="comment odd alt depth-2">
			<article id="div-comment-643102" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/02994aa7c2331aee71a5a443ba3b7fb0.png" srcset="https://secure.gravatar.com/avatar/02994aa7c2331aee71a5a443ba3b7fb0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">mdg1019</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-643102">
								<time datetime="2021-07-08T13:26:08+00:00" itemprop="datePublished">
									July 8, 2021 at 1:26 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>I believe you can do what you want with the WifFi.softAPConfig() function.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=643102#respond" data-commentid="643102" data-postid="67766" data-belowelement="div-comment-643102" data-respondelement="respond" data-replyto="Reply to mdg1019" aria-label="Reply to mdg1019">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-341366" class="comment even thread-odd thread-alt depth-1 parent">
			<article id="div-comment-341366" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e72d1bc5ffe0673bc9e996c4fe2425c6.png" srcset="https://secure.gravatar.com/avatar/e72d1bc5ffe0673bc9e996c4fe2425c6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Alan Cross</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-341366">
								<time datetime="2018-10-29T14:20:15+00:00" itemprop="datePublished">
									October 29, 2018 at 2:20 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi guys, just want to say a great tutorial. I have a Heltec ESP32 with OLED display and have the web server up and running in both AP and STA modes. Works like a treat. I have the OLED display the text status of 3 of the output pins (one of which is the on-board LED Pin25).<br>
I have added a third button which was very easy. Also changed the size &amp; colour of the buttons.<br>
Great stuff!!</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=341366#respond" data-commentid="341366" data-postid="67766" data-belowelement="div-comment-341366" data-respondelement="respond" data-replyto="Reply to Alan Cross" aria-label="Reply to Alan Cross">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-341817" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2">
			<article id="div-comment-341817" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-341817">
								<time datetime="2018-11-01T11:18:22+00:00" itemprop="datePublished">
									November 1, 2018 at 11:18 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Alan!<br>
That’s great! Keep up the good work!<br>
Regards,<br>
Sara <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=341817#respond" data-commentid="341817" data-postid="67766" data-belowelement="div-comment-341817" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-362784" class="comment even depth-2">
			<article id="div-comment-362784" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/2c2244f1caf00a13790b9f8f4990ef19.png" srcset="https://secure.gravatar.com/avatar/2c2244f1caf00a13790b9f8f4990ef19?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Pablo</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-362784">
								<time datetime="2019-04-19T14:39:50+00:00" itemprop="datePublished">
									April 19, 2019 at 2:39 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hola, Alan por favor puedes compartir tu codigo, estoy tratanto de hacer lo mismo, gracias</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=362784#respond" data-commentid="362784" data-postid="67766" data-belowelement="div-comment-362784" data-respondelement="respond" data-replyto="Reply to Pablo" aria-label="Reply to Pablo">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-342414" class="comment odd alt thread-even depth-1 parent">
			<article id="div-comment-342414" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/5a54a11bcc4f00fa0c30565466e432dc.png" srcset="https://secure.gravatar.com/avatar/5a54a11bcc4f00fa0c30565466e432dc?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Musi Mumu</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-342414">
								<time datetime="2018-11-05T10:34:53+00:00" itemprop="datePublished">
									November 5, 2018 at 10:34 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Sara<br>
Esp 32 can show when a phone is connected to ap<br>
If yes please help<br>
Regards</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=342414#respond" data-commentid="342414" data-postid="67766" data-belowelement="div-comment-342414" data-respondelement="respond" data-replyto="Reply to Musi Mumu" aria-label="Reply to Musi Mumu">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-342900" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-342900" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-342900">
								<time datetime="2018-11-08T09:53:30+00:00" itemprop="datePublished">
									November 8, 2018 at 9:53 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Musi,<br>
When the ESP32 is set as an access point, when you connect your smartphone to the ESP32, you are connected to the ESP32 network.<br>
So, you can’t access apps that require data network.<br>
Regards,<br>
Sara <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=342900#respond" data-commentid="342900" data-postid="67766" data-belowelement="div-comment-342900" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-351413" class="comment odd alt thread-odd thread-alt depth-1">
			<article id="div-comment-351413" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/62058cf699e8e656e57e735cf49f2e9b.png" srcset="https://secure.gravatar.com/avatar/62058cf699e8e656e57e735cf49f2e9b?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn"><a href="http://kio4.com/arduino/119_Wemos_PuntoAcceso_BotonLED.htm" rel="external nofollow ugc" class="url">Juan Antonio</a></cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-351413">
								<time datetime="2019-01-03T14:49:14+00:00" itemprop="datePublished">
									January 3, 2019 at 2:49 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Maybe changing int max_connection = 4<br>
you can get more connections. I have not tried it.</p>
<p><a href="https://github.com/espressif/arduino-esp32/blob/master/libraries/WiFi/src/WiFiAP.h" rel="nofollow ugc">https://github.com/espressif/arduino-esp32/blob/master/libraries/WiFi/src/WiFiAP.h</a></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=351413#respond" data-commentid="351413" data-postid="67766" data-belowelement="div-comment-351413" data-respondelement="respond" data-replyto="Reply to Juan Antonio" aria-label="Reply to Juan Antonio">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-354772" class="comment even thread-even depth-1 parent">
			<article id="div-comment-354772" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/3cacb911dd1499c49c3ba95e3707382d.png" srcset="https://secure.gravatar.com/avatar/3cacb911dd1499c49c3ba95e3707382d?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Chris</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-354772">
								<time datetime="2019-02-02T20:29:14+00:00" itemprop="datePublished">
									February 2, 2019 at 8:29 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Thank your for a very thorough tutorial.<br>
 I am having problems getting it to work on IOS devices. I works fine on Win 10 and Android devices. If I try to connect with  a IOS 12 phone it wont connect and in the device ip address it does not list the expected 192.168.4.1 address. If I modify the source code to not pass the password parameter. IE an open network it connects as expected. I have tried similar examples from other sites and they produce similar results.<br>
I would be grateful if you could give me any help as how to proceed with debugging the problem. I am using esp32 and using the code you supply.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=354772#respond" data-commentid="354772" data-postid="67766" data-belowelement="div-comment-354772" data-respondelement="respond" data-replyto="Reply to Chris" aria-label="Reply to Chris">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-355004" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2 parent">
			<article id="div-comment-355004" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-355004">
								<time datetime="2019-02-05T09:55:41+00:00" itemprop="datePublished">
									February 5, 2019 at 9:55 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Chris.<br>
That’s very weird and I have no idea why that is happening.<br>
It may be something related with your phone.<br>
Other people reported issues about connecting with other phones, but I don’t know what the reason is.<br>
I’ve searched on the internet and haven’t found a clear answer.<br>
I found this issue on the forum, but it doesn’t have an answer yet: github.com/espressif/arduino-esp32/issues/2242<br>
It is a problem similar to yours.<br>
Sorry that I can’t help much.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=355004#respond" data-commentid="355004" data-postid="67766" data-belowelement="div-comment-355004" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-355042" class="comment even depth-3">
			<article id="div-comment-355042" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1164a1214160fa30b9a7cabb352ae0aa.jpeg" srcset="https://secure.gravatar.com/avatar/1164a1214160fa30b9a7cabb352ae0aa?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Duncan Amos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-355042">
								<time datetime="2019-02-05T14:12:21+00:00" itemprop="datePublished">
									February 5, 2019 at 2:12 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>My understanding (which could be wrong) is that iOS, and some other phones, won’t connect unless there is an onward connection to the Internet.</p>
<p>This has caused me unresolved problems with Raspberry Pi based devices.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=355042#respond" data-commentid="355042" data-postid="67766" data-belowelement="div-comment-355042" data-respondelement="respond" data-replyto="Reply to Duncan Amos" aria-label="Reply to Duncan Amos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-355119" class="comment odd alt thread-odd thread-alt depth-1">
			<article id="div-comment-355119" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/3cacb911dd1499c49c3ba95e3707382d.png" srcset="https://secure.gravatar.com/avatar/3cacb911dd1499c49c3ba95e3707382d?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Chris</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-355119">
								<time datetime="2019-02-06T11:09:27+00:00" itemprop="datePublished">
									February 6, 2019 at 11:09 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Thanks any way for taking the time to reply. It seems it may be a problem with IOS rather than the ESP side of things. If I find an answer I will let you know <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"></p>
<p>Thanks again for a very informative site.</p>
<p>Regards from Chris.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=355119#respond" data-commentid="355119" data-postid="67766" data-belowelement="div-comment-355119" data-respondelement="respond" data-replyto="Reply to Chris" aria-label="Reply to Chris">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-360276" class="comment even thread-even depth-1 parent">
			<article id="div-comment-360276" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/bd421b781489d5720355ebb55bdc89fe.png" srcset="https://secure.gravatar.com/avatar/bd421b781489d5720355ebb55bdc89fe?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Ricardo</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-360276">
								<time datetime="2019-03-30T12:56:48+00:00" itemprop="datePublished">
									March 30, 2019 at 12:56 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Greetings;</p>
<p>I’m still understanding the code and procedures.<br>
1 Question: Is it possible to configure Wifi Encryption?</p>
<p>Something like: </p>
<p>byte encryption = 2;</p>
<p>    TKIP (WPA) = 2<br>
    // WEP = 5<br>
    // CCMP (WPA) = 4<br>
    // NONE = 7<br>
    // AUTO = 8 </p>
<p>Both WiFi and WiFiAp classes dont have a way to set this; but I’ve read that it is possible.<br>
Thanks in advance.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=360276#respond" data-commentid="360276" data-postid="67766" data-belowelement="div-comment-360276" data-respondelement="respond" data-replyto="Reply to Ricardo" aria-label="Reply to Ricardo">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-360431" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2">
			<article id="div-comment-360431" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-360431">
								<time datetime="2019-03-31T15:52:36+00:00" itemprop="datePublished">
									March 31, 2019 at 3:52 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Ricardo,<br>
Unfortunately, we don’t have any tutorials about that subject.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=360431#respond" data-commentid="360431" data-postid="67766" data-belowelement="div-comment-360431" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-361367" class="comment even thread-odd thread-alt depth-1 parent">
			<article id="div-comment-361367" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/a2ef73541a0b2102d9dd0a87b368b91f.png" srcset="https://secure.gravatar.com/avatar/a2ef73541a0b2102d9dd0a87b368b91f?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Bryan</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-361367">
								<time datetime="2019-04-09T07:01:31+00:00" itemprop="datePublished">
									April 9, 2019 at 7:01 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Sara, thanks for all your tutorials on this website, they are very clear and well done! </p>
<p>After setting my ESP32 as an access point, can I send data from this one?<br>
I mean I’d like to send the data from a sensor connected to my ESP32 and reading them on my phone or tablet.</p>
<p>Thanks.</p>
<p>Bryan</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=361367#respond" data-commentid="361367" data-postid="67766" data-belowelement="div-comment-361367" data-respondelement="respond" data-replyto="Reply to Bryan" aria-label="Reply to Bryan">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-362666" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2">
			<article id="div-comment-362666" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-362666">
								<time datetime="2019-04-18T15:40:31+00:00" itemprop="datePublished">
									April 18, 2019 at 3:40 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Bryan.<br>
Yes, you can do that. It works like any other web server we have in our tutorials. But instead of connecting to your local network to get the readings, you connect to the ESP32 access point.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=362666#respond" data-commentid="362666" data-postid="67766" data-belowelement="div-comment-362666" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-363730" class="comment even thread-even depth-1 parent">
			<article id="div-comment-363730" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/9daedb38ad201e0f65beaf7818248316.png" srcset="https://secure.gravatar.com/avatar/9daedb38ad201e0f65beaf7818248316?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">joao silva</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-363730">
								<time datetime="2019-04-27T20:55:12+00:00" itemprop="datePublished">
									April 27, 2019 at 8:55 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>O was trying to set an esp32 cam as an access point, so i could see the vídeo stream, with no need to connect to the router…but no luck yet…maybe you guys could lend a hand<img draggable="false" role="img" class="emoji" alt="😉" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f609.svg"></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=363730#respond" data-commentid="363730" data-postid="67766" data-belowelement="div-comment-363730" data-respondelement="respond" data-replyto="Reply to joao silva" aria-label="Reply to joao silva">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-363822" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2 parent">
			<article id="div-comment-363822" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-363822">
								<time datetime="2019-04-28T13:07:01+00:00" itemprop="datePublished">
									April 28, 2019 at 1:07 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi João.<br>
What is the exact problem that you’re facing?<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=363822#respond" data-commentid="363822" data-postid="67766" data-belowelement="div-comment-363822" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-363831" class="comment even depth-3">
			<article id="div-comment-363831" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/9daedb38ad201e0f65beaf7818248316.png" srcset="https://secure.gravatar.com/avatar/9daedb38ad201e0f65beaf7818248316?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">joao silva</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-363831">
								<time datetime="2019-04-28T13:51:01+00:00" itemprop="datePublished">
									April 28, 2019 at 1:51 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Well..the main problem are my poor programing skills…<img draggable="false" role="img" class="emoji" alt="😣" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f623.svg"><br>
Appart from that i’m trying to make a sort of a standalone WiFi câmera on the cheap…that you could hide in common everyday objects…and that could be accessed on and Android phone..wich could store the stream if wanted..<br>
.it seems a good project for the esp32 and android app development…<br>
Are you interested in helping</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=363831#respond" data-commentid="363831" data-postid="67766" data-belowelement="div-comment-363831" data-respondelement="respond" data-replyto="Reply to joao silva" aria-label="Reply to joao silva">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-365983" class="comment odd alt thread-odd thread-alt depth-1">
			<article id="div-comment-365983" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/c3e0c389e41d10285e86233b81e5dd4d.png" srcset="https://secure.gravatar.com/avatar/c3e0c389e41d10285e86233b81e5dd4d?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Tim</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-365983">
								<time datetime="2019-05-14T20:32:00+00:00" itemprop="datePublished">
									May 14, 2019 at 8:32 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Thx soo much for posting this – just what I needed and works like a charm !<br>
You’re a star !</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=365983#respond" data-commentid="365983" data-postid="67766" data-belowelement="div-comment-365983" data-respondelement="respond" data-replyto="Reply to Tim" aria-label="Reply to Tim">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-382850" class="comment even thread-even depth-1">
			<article id="div-comment-382850" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/5a54a11bcc4f00fa0c30565466e432dc.png" srcset="https://secure.gravatar.com/avatar/5a54a11bcc4f00fa0c30565466e432dc?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Musi Mumu</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-382850">
								<time datetime="2019-06-25T10:30:59+00:00" itemprop="datePublished">
									June 25, 2019 at 10:30 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>It is known that max_connection” limitations is 4 for ESP8266 and 32<br>
Also is known that for 8266 can be extend to 8 and for 32 even more<br>
Can you help me for doing this</p>
<p>Regards</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=382850#respond" data-commentid="382850" data-postid="67766" data-belowelement="div-comment-382850" data-respondelement="respond" data-replyto="Reply to Musi Mumu" aria-label="Reply to Musi Mumu">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-383887" class="comment odd alt thread-odd thread-alt depth-1">
			<article id="div-comment-383887" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/5a54a11bcc4f00fa0c30565466e432dc.png" srcset="https://secure.gravatar.com/avatar/5a54a11bcc4f00fa0c30565466e432dc?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Musi Mumu</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-383887">
								<time datetime="2019-07-05T16:28:26+00:00" itemprop="datePublished">
									July 5, 2019 at 4:28 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>You say that  ” there are also other optional parameters you can pass to the softAP() method. Here’s all the parameters:”<br>
max_connection: maximum simultaneous connected clients (1-4)<br>
Haw to program softAP to accept 8 or more simultaneous connected clients<br>
Will be very useful if you will make a tutorial or help me to do that.<br>
Best regards</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=383887#respond" data-commentid="383887" data-postid="67766" data-belowelement="div-comment-383887" data-respondelement="respond" data-replyto="Reply to Musi Mumu" aria-label="Reply to Musi Mumu">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-385393" class="comment even thread-even depth-1">
			<article id="div-comment-385393" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/bf0afbde3c86d3267b02112e34008b2a.jpeg" srcset="https://secure.gravatar.com/avatar/bf0afbde3c86d3267b02112e34008b2a?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Vitaly</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-385393">
								<time datetime="2019-07-23T15:33:04+00:00" itemprop="datePublished">
									July 23, 2019 at 3:33 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>If some phones won’t connect – just disable mobile communication, worked for me. Thanks for the tutorial</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=385393#respond" data-commentid="385393" data-postid="67766" data-belowelement="div-comment-385393" data-respondelement="respond" data-replyto="Reply to Vitaly" aria-label="Reply to Vitaly">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-418607" class="comment odd alt thread-odd thread-alt depth-1">
			<article id="div-comment-418607" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/7af59654a2d6f4c9ad25588920c4edff.png" srcset="https://secure.gravatar.com/avatar/7af59654a2d6f4c9ad25588920c4edff?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Noel Silva</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-418607">
								<time datetime="2020-01-02T17:31:54+00:00" itemprop="datePublished">
									January 2, 2020 at 5:31 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Good afternoon, SARA<br>
For me it worked round, just need to find a server to host.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=418607#respond" data-commentid="418607" data-postid="67766" data-belowelement="div-comment-418607" data-respondelement="respond" data-replyto="Reply to Noel Silva" aria-label="Reply to Noel Silva">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-421801" class="comment even thread-even depth-1">
			<article id="div-comment-421801" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/3f18dfdfde79e034eff455a6a2b59ee0.png" srcset="https://secure.gravatar.com/avatar/3f18dfdfde79e034eff455a6a2b59ee0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Dave K.</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-421801">
								<time datetime="2020-01-15T16:48:21+00:00" itemprop="datePublished">
									January 15, 2020 at 4:48 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Ok, so I’m a little bit behind (Ha!)….but, none the less, this is a great project!</p>
<p>This morning I put it together with a DS18B20, added a 3rd button to the webpage and temperature readout. VERY COOL!</p>
<p>Hopefully I can add a Si7021 on I2C and display that as well in the near future. This saves so much other work! All I need to do is drop my solar battery to a 5V level with a switching module, hook it up to the dev board, and bam! remote access, monitoring, and control! Wow!</p>
<p>I LOVE RNT!!!</p>
<p>Thanks so much for your projects and inspirations!<br>
Best Always!<br>
Dave</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=421801#respond" data-commentid="421801" data-postid="67766" data-belowelement="div-comment-421801" data-respondelement="respond" data-replyto="Reply to Dave K." aria-label="Reply to Dave K.">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-429563" class="comment odd alt thread-odd thread-alt depth-1 parent">
			<article id="div-comment-429563" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/839b130531b96c4f24ed170aa4119573.png" srcset="https://secure.gravatar.com/avatar/839b130531b96c4f24ed170aa4119573?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Dan</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-429563">
								<time datetime="2020-02-15T18:25:20+00:00" itemprop="datePublished">
									February 15, 2020 at 6:25 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>I’m searching for a way to send “time” to 6 stations mostly ESP-01s (I may use other board if useful ) from a server like ESP32. Not using my local network nor using the net. Just to send the time to all the stations at the same time. Not need to receive any data from those stations. Do you have a good direction on how to do it. What I see on the net is always the reverse like Stations sending to the Server. I don’t want to use UDP as it’s not safe. Many thanks for your help. 02-15-2020</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=429563#respond" data-commentid="429563" data-postid="67766" data-belowelement="div-comment-429563" data-respondelement="respond" data-replyto="Reply to Dan" aria-label="Reply to Dan">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-429573" class="comment byuser comment-author-sara-santos bypostauthor even depth-2 parent">
			<article id="div-comment-429573" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-429573">
								<time datetime="2020-02-15T19:17:24+00:00" itemprop="datePublished">
									February 15, 2020 at 7:17 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Dan.<br>
You can use ESPNOW to send messages to multiple boards. We have tutorials for ESPNOW with ESP32:<br>
– <a href="https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/" rel="nofollow ugc">https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/</a><br>
– <a href="https://randomnerdtutorials.com/esp-now-two-way-communication-esp32/" rel="nofollow ugc">https://randomnerdtutorials.com/esp-now-two-way-communication-esp32/</a><br>
Next week, we’ll be publishing a tutorial about ESP-NOW with the ESP8266.<br>
You can make an ESP32 and ESP8266 communicate with each other using ESP-NOW.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=429573#respond" data-commentid="429573" data-postid="67766" data-belowelement="div-comment-429573" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-429876" class="comment odd alt depth-3">
			<article id="div-comment-429876" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/839b130531b96c4f24ed170aa4119573.png" srcset="https://secure.gravatar.com/avatar/839b130531b96c4f24ed170aa4119573?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Dan</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-429876">
								<time datetime="2020-02-16T23:45:47+00:00" itemprop="datePublished">
									February 16, 2020 at 11:45 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hey!!! that’s what I need, finally. And If I may, my optimal setup would be to use all ESP-01s with a Pic from microchip as all my thermostat setup is almost done with PIC. And if possible in a near future I may need to access my local network to change some settings in the master thermostat using my computer, but without being able to go on the net for safety reasons. So if you can give us some details on how to do it I’m sure that it will be useful to others.<br>
Thanks for your help.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=429876#respond" data-commentid="429876" data-postid="67766" data-belowelement="div-comment-429876" data-respondelement="respond" data-replyto="Reply to Dan" aria-label="Reply to Dan">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-444317" class="comment even thread-even depth-1 parent">
			<article id="div-comment-444317" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/4503cf51ff188c39b2ea7c3e1f7b2c33.jpeg" srcset="https://secure.gravatar.com/avatar/4503cf51ff188c39b2ea7c3e1f7b2c33?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Ykn3</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-444317">
								<time datetime="2020-04-08T06:42:42+00:00" itemprop="datePublished">
									April 8, 2020 at 6:42 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>I really like this tutorial, but I am having a problem with it. Everything is going well until I disconnect the wifi from my pc and try to reconnect, then my page breake and cannot reconnect. It’s a big problem for code applications, since i can’t get  very far from the project after I start running the code without losing my connection. I can’t be reseting the Esp32 fisicaly, and the only way i find to repair it, is rebooting. I’m not a professional programmer and, unfortunately, I still haven’t found a solution for that. If anyone knows how to enable it can be connected and disconnected from wifi without problems, please help me. I’m already happy for the post, but this help can make it even more interesting. thanks</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=444317#respond" data-commentid="444317" data-postid="67766" data-belowelement="div-comment-444317" data-respondelement="respond" data-replyto="Reply to Ykn3" aria-label="Reply to Ykn3">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-444363" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2">
			<article id="div-comment-444363" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-444363">
								<time datetime="2020-04-08T09:29:31+00:00" itemprop="datePublished">
									April 8, 2020 at 9:29 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
Thanks for your comment.<br>
Do you want to software reboot the ESP32 remotely?<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=444363#respond" data-commentid="444363" data-postid="67766" data-belowelement="div-comment-444363" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-573141" class="comment even depth-2">
			<article id="div-comment-573141" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/0d466c2c51fa193a6c5313eefade3176.png" srcset="https://secure.gravatar.com/avatar/0d466c2c51fa193a6c5313eefade3176?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">hexdump</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-573141">
								<time datetime="2021-03-16T08:40:02+00:00" itemprop="datePublished">
									March 16, 2021 at 8:40 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi. I have the same problem. Everything works OK until I disconnect from the AP. Then the pages will no longer appear. It is necessary to restart the module</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=573141#respond" data-commentid="573141" data-postid="67766" data-belowelement="div-comment-573141" data-respondelement="respond" data-replyto="Reply to hexdump" aria-label="Reply to hexdump">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-454284" class="comment odd alt thread-odd thread-alt depth-1 parent">
			<article id="div-comment-454284" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/4cf83b025e9fdd260a856c05ace771db.png" srcset="https://secure.gravatar.com/avatar/4cf83b025e9fdd260a856c05ace771db?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Col</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-454284">
								<time datetime="2020-05-07T12:26:03+00:00" itemprop="datePublished">
									May 7, 2020 at 12:26 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hello Rui &amp; Sara<br>
Thanks – great work<br>
I cannot get soft AP mode to work with the RTOS, do you know any reason for this ?</p>
<p>Thanks Hb</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=454284#respond" data-commentid="454284" data-postid="67766" data-belowelement="div-comment-454284" data-respondelement="respond" data-replyto="Reply to Col" aria-label="Reply to Col">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-454561" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-454561" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-454561">
								<time datetime="2020-05-08T10:06:11+00:00" itemprop="datePublished">
									May 8, 2020 at 10:06 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
What do you mean?<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=454561#respond" data-commentid="454561" data-postid="67766" data-belowelement="div-comment-454561" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-460963" class="comment odd alt thread-even depth-1">
			<article id="div-comment-460963" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/19d183ba076f7617063e8c14ea215362.png" srcset="https://secure.gravatar.com/avatar/19d183ba076f7617063e8c14ea215362?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Naenon</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-460963">
								<time datetime="2020-05-28T02:47:57+00:00" itemprop="datePublished">
									May 28, 2020 at 2:47 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Thank you , now i can do that.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=460963#respond" data-commentid="460963" data-postid="67766" data-belowelement="div-comment-460963" data-respondelement="respond" data-replyto="Reply to Naenon" aria-label="Reply to Naenon">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-465939" class="comment even thread-odd thread-alt depth-1 parent">
			<article id="div-comment-465939" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/cf894f7e51f3c1945f44eb5771b18663.png" srcset="https://secure.gravatar.com/avatar/cf894f7e51f3c1945f44eb5771b18663?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Alistair McKinnon</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-465939">
								<time datetime="2020-06-13T10:29:34+00:00" itemprop="datePublished">
									June 13, 2020 at 10:29 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Great tutorial as always.<br>
Is there a way of using Soft Access Point with ESP32 Cam, to stream video from ESP32 Cam to Phone/tablet without using Router?</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=465939#respond" data-commentid="465939" data-postid="67766" data-belowelement="div-comment-465939" data-respondelement="respond" data-replyto="Reply to Alistair McKinnon" aria-label="Reply to Alistair McKinnon">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-467044" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2 parent">
			<article id="div-comment-467044" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-467044">
								<time datetime="2020-06-16T20:43:21+00:00" itemprop="datePublished">
									June 16, 2020 at 8:43 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Yes.<br>
Just follow this tutorial.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=467044#respond" data-commentid="467044" data-postid="67766" data-belowelement="div-comment-467044" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-467640" class="comment even depth-3">
			<article id="div-comment-467640" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/cf894f7e51f3c1945f44eb5771b18663.png" srcset="https://secure.gravatar.com/avatar/cf894f7e51f3c1945f44eb5771b18663?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Alistair</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-467640">
								<time datetime="2020-06-18T23:47:48+00:00" itemprop="datePublished">
									June 18, 2020 at 11:47 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Many thanks, that’s great.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=467640#respond" data-commentid="467640" data-postid="67766" data-belowelement="div-comment-467640" data-respondelement="respond" data-replyto="Reply to Alistair" aria-label="Reply to Alistair">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-465973" class="comment odd alt thread-even depth-1 parent">
			<article id="div-comment-465973" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/9f43d525f696cfebbd82037a5628cd17.png" srcset="https://secure.gravatar.com/avatar/9f43d525f696cfebbd82037a5628cd17?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Berguinsson</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-465973">
								<time datetime="2020-06-13T12:44:03+00:00" itemprop="datePublished">
									June 13, 2020 at 12:44 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Rui and Sara.<br>
Perhaps this is a network concept rather than a esp32 concept, but i think thath you could help me…<br>
If the ESP32 is the Acces Point, i’m able to connect my laptop to its own network , right?<br>
And usign its own network can i acces to any web page like it was the normal router network? How is it possible?<br>
I understand that the router is connected by wire to the global network, for this reason when i connect a device to the router wifi i can go to any web page of the world.<br>
Instead, how the information of any web page can arrive to my laptop through the ESP32 network, if this ESP32 is not connected to the global network?</p>
<p>It is more a conceptual doubt than a software/hardware doubt.</p>
<p>I’m looking forward to hearing from you!</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=465973#respond" data-commentid="465973" data-postid="67766" data-belowelement="div-comment-465973" data-respondelement="respond" data-replyto="Reply to Berguinsson" aria-label="Reply to Berguinsson">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-466011" class="comment even depth-2">
			<article id="div-comment-466011" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1164a1214160fa30b9a7cabb352ae0aa.jpeg" srcset="https://secure.gravatar.com/avatar/1164a1214160fa30b9a7cabb352ae0aa?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Duncan Amos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-466011">
								<time datetime="2020-06-13T14:43:41+00:00" itemprop="datePublished">
									June 13, 2020 at 2:43 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>You have misunderstood.</p>
<p>You would be able to access a webpage that is hosted on the ESP-32 only – you would not have access to webpages on the Internet.</p>
<p>It can be useful to have a locally hosted webpage to supply specific information. If you have regular visitors, for instance, you could have the webpage show local buildings of interest and their history, things like that.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=466011#respond" data-commentid="466011" data-postid="67766" data-belowelement="div-comment-466011" data-respondelement="respond" data-replyto="Reply to Duncan Amos" aria-label="Reply to Duncan Amos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-489134" class="comment odd alt thread-odd thread-alt depth-1 parent">
			<article id="div-comment-489134" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e5b47fcdfe0f1bbffb92cbc4e5293938.png" srcset="https://secure.gravatar.com/avatar/e5b47fcdfe0f1bbffb92cbc4e5293938?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Graham Martin</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-489134">
								<time datetime="2020-08-21T20:18:51+00:00" itemprop="datePublished">
									August 21, 2020 at 8:18 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi, a bit late to the party I know. I found your article very helpful and very informative to a<br>
serious newbie at this programming stuff.<br>
Using your code got me running an esp32-cam as an access point and with a simple aerial I can get ~200m which is perfect for my needs.<br>
I would like to use multiple cameras each with their own SSID and IP address, the SSID is obvious but I have no idea how to get a different IP on each camera AP.</p>
<p>Can anyone point me in the right direction?</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=489134#respond" data-commentid="489134" data-postid="67766" data-belowelement="div-comment-489134" data-respondelement="respond" data-replyto="Reply to Graham Martin" aria-label="Reply to Graham Martin">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-489275" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-489275" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-489275">
								<time datetime="2020-08-22T08:23:32+00:00" itemprop="datePublished">
									August 22, 2020 at 8:23 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
To assign a specific IP address to a board, you can follow this tutorial: <a href="https://randomnerdtutorials.com/esp32-static-fixed-ip-address-arduino-ide/" rel="nofollow ugc">https://randomnerdtutorials.com/esp32-static-fixed-ip-address-arduino-ide/</a><br>
I hope this helps.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=489275#respond" data-commentid="489275" data-postid="67766" data-belowelement="div-comment-489275" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-489343" class="comment odd alt thread-even depth-1 parent">
			<article id="div-comment-489343" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e5b47fcdfe0f1bbffb92cbc4e5293938.png" srcset="https://secure.gravatar.com/avatar/e5b47fcdfe0f1bbffb92cbc4e5293938?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Graham Martin</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-489343">
								<time datetime="2020-08-22T12:41:16+00:00" itemprop="datePublished">
									August 22, 2020 at 12:41 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Sara,<br>
 Thanks so much for the prompt reply,<br>
Your static IP tutorial sets a fixed IP address to the esp32 when connecting to, say, my home network 192.168.1.xxx, what I need is to be able to control the IP address that the esp32 issues (DHCP), when acting as an access point, in the one I have done so far from your tutorial, 192.168.4.1. I intend to have six cameras close to one another and need to be able to connect to any of then individually.<br>
It occurs to me that the SSID might perform this function in a way, all cameras being on a separate network?</p>
<p>Thanks again Graham</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=489343#respond" data-commentid="489343" data-postid="67766" data-belowelement="div-comment-489343" data-respondelement="respond" data-replyto="Reply to Graham Martin" aria-label="Reply to Graham Martin">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-489931" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-489931" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-489931">
								<time datetime="2020-08-24T05:30:53+00:00" itemprop="datePublished">
									August 24, 2020 at 5:30 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
Yes, because they are on a different network, you can connect to them separately.<br>
They will all have the 192.168.4.1 address, but because they are on different networks, you can connect to them separately.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=489931#respond" data-commentid="489931" data-postid="67766" data-belowelement="div-comment-489931" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-490507" class="comment odd alt thread-odd thread-alt depth-1 parent">
			<article id="div-comment-490507" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e158dc0844cbc9d1f57ef9fc39826a79.png" srcset="https://secure.gravatar.com/avatar/e158dc0844cbc9d1f57ef9fc39826a79?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Bob Martin</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-490507">
								<time datetime="2020-08-25T18:58:13+00:00" itemprop="datePublished">
									August 25, 2020 at 6:58 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>I have the soft AP server running on an ESP32_CAM with a battery, a 3.3V regulator and an external antenna. It works fine when the serial cable is attached but stops updating  images when it is removed.</p>
<p>If I touch the serial port pins with my hand, it starts again and stops as soon as I remove my hand..  Touching other pins on side of  the ESP32 CAM board with the serial port also keeps it running.  Touching pins on the other edge of the board does not appear to have this effect.  Any thoughts on this mystery?</p>
<p>Thanks,</p>
<p>Bob</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=490507#respond" data-commentid="490507" data-postid="67766" data-belowelement="div-comment-490507" data-respondelement="respond" data-replyto="Reply to Bob Martin" aria-label="Reply to Bob Martin">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-490850" class="comment byuser comment-author-sara-santos bypostauthor even depth-2 parent">
			<article id="div-comment-490850" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-490850">
								<time datetime="2020-08-26T16:53:48+00:00" itemprop="datePublished">
									August 26, 2020 at 4:53 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Bob.<br>
Which pins are you using to power the ESP32-CAM?<br>
Can you provide more details?<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=490850#respond" data-commentid="490850" data-postid="67766" data-belowelement="div-comment-490850" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-490902" class="comment odd alt depth-3 parent">
			<article id="div-comment-490902" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/e158dc0844cbc9d1f57ef9fc39826a79.png" srcset="https://secure.gravatar.com/avatar/e158dc0844cbc9d1f57ef9fc39826a79?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Robert Martin</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-490902">
								<time datetime="2020-08-26T19:26:20+00:00" itemprop="datePublished">
									August 26, 2020 at 7:26 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Sara,</p>
<p>I did send an update to Rui but I’ll post it here along with some added info.<br>
 I submitted a post yesterday about intermittent operation of the<br>
ESP32-CAM that involved touching the serial port pins to get it working.</p>
<p>The problem appears to be fixed but you might want to remember this<br>
for future reference given that you are the repository for all things ESP32.</p>
<p>I had glued the external antenna to the end of the ESP32-CAM along the edge with the internal antenna and experienced the problems.</p>
<p>Breaking the glue joint and moving the antenna a small distance away<br>
from the ESP32_CAM fixed the problem. . I further experimented and could get occasional image updates  depending on where I placed my hands near the antenna.</p>
<p>My assumption is that RF energy from the WiFi antenna was getting picked up and upsetting the operation but not crashing the system since it always resumed working when I touched the pins.</p>
<p>Now here is where it gets (more) interesting. I popped an ESP32-CAM with internal antenna into my test fixture and saw exactly the same problem except that I couldn’t move the antenna away as it was built-in.</p>
<p>Next I put a .1uF capacitor between the 3.3V pin and the nearest ground<br>
which was three pins over and the problem went away.</p>
<p>I think mounting the ESP32-CAM on a good board with a ground plane along with bypassing the 3.3V pin may help those who are having issues running off 3.3V.</p>
<p>Best Regards,</p>
<p>Bob</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=490902#respond" data-commentid="490902" data-postid="67766" data-belowelement="div-comment-490902" data-respondelement="respond" data-replyto="Reply to Robert Martin" aria-label="Reply to Robert Martin">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-491232" class="comment byuser comment-author-sara-santos bypostauthor even depth-4">
			<article id="div-comment-491232" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-491232">
								<time datetime="2020-08-27T17:27:17+00:00" itemprop="datePublished">
									August 27, 2020 at 5:27 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Thanks for sharing this.<br>
It may be useful for our readers.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=491232#respond" data-commentid="491232" data-postid="67766" data-belowelement="div-comment-491232" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-504767" class="comment odd alt thread-even depth-1">
			<article id="div-comment-504767" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/856904b9921803891b9e540a720d6117.png" srcset="https://secure.gravatar.com/avatar/856904b9921803891b9e540a720d6117?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn"><a href="http://www.oficinadalmada.org/" rel="external nofollow ugc" class="url">João Catarino</a></cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-504767">
								<time datetime="2020-10-09T22:28:32+00:00" itemprop="datePublished">
									October 9, 2020 at 10:28 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi there, is there a way of, while having the AP mode, make it redirect to the page automatically, like it does with the Captive Portal example?</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=504767#respond" data-commentid="504767" data-postid="67766" data-belowelement="div-comment-504767" data-respondelement="respond" data-replyto="Reply to João Catarino" aria-label="Reply to João Catarino">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-508182" class="comment even thread-odd thread-alt depth-1">
			<article id="div-comment-508182" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/ed061d5e59f21ed659ad54b8a32b7248.png" srcset="https://secure.gravatar.com/avatar/ed061d5e59f21ed659ad54b8a32b7248?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Mark Phillips</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-508182">
								<time datetime="2020-10-20T01:59:00+00:00" itemprop="datePublished">
									October 20, 2020 at 1:59 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>The code works great <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"> I have my ESP32 setup as an Access Point.<br>
My issue is when I have my smart phone or pc connected and then leave the house and come back and reconnect to my ESP, the webpage will not refresh unless I reset the ESP and reconnect</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=508182#respond" data-commentid="508182" data-postid="67766" data-belowelement="div-comment-508182" data-respondelement="respond" data-replyto="Reply to Mark Phillips" aria-label="Reply to Mark Phillips">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-510637" class="comment odd alt thread-even depth-1 parent">
			<article id="div-comment-510637" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/dfaefce717703aea35522e377a2519e8.png" srcset="https://secure.gravatar.com/avatar/dfaefce717703aea35522e377a2519e8?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">José Toscano</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-510637">
								<time datetime="2020-10-26T16:11:02+00:00" itemprop="datePublished">
									October 26, 2020 at 4:11 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Rui &amp; Sara,<br>
This is great work, thank you for guide us.<br>
I made it work <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"> However, I need to make the process totally automatic. I need to push the file to the ESP32 without having to open the browser, entering the site, define the file, and clicking the button to start the upload. Is this possible?<br>
Thank you in advance</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=510637#respond" data-commentid="510637" data-postid="67766" data-belowelement="div-comment-510637" data-respondelement="respond" data-replyto="Reply to José Toscano" aria-label="Reply to José Toscano">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-510761" class="comment byuser comment-author-sara-santos bypostauthor even depth-2 parent">
			<article id="div-comment-510761" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-510761">
								<time datetime="2020-10-26T23:05:53+00:00" itemprop="datePublished">
									October 26, 2020 at 11:05 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
Search for “OTA programming” with the ESP32.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=510761#respond" data-commentid="510761" data-postid="67766" data-belowelement="div-comment-510761" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-510963" class="comment odd alt depth-3">
			<article id="div-comment-510963" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/dfaefce717703aea35522e377a2519e8.png" srcset="https://secure.gravatar.com/avatar/dfaefce717703aea35522e377a2519e8?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">José Toscano</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-510963">
								<time datetime="2020-10-27T11:03:31+00:00" itemprop="datePublished">
									October 27, 2020 at 11:03 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Thanks Sara.<br>
BR</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=510963#respond" data-commentid="510963" data-postid="67766" data-belowelement="div-comment-510963" data-respondelement="respond" data-replyto="Reply to José Toscano" aria-label="Reply to José Toscano">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-530465" class="comment even thread-odd thread-alt depth-1 parent">
			<article id="div-comment-530465" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1318b1efa25bb533abbc4243249a67a2.png" srcset="https://secure.gravatar.com/avatar/1318b1efa25bb533abbc4243249a67a2?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Asad Shaikh</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-530465">
								<time datetime="2020-12-18T03:12:38+00:00" itemprop="datePublished">
									December 18, 2020 at 3:12 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Can we used physical push button in ESP32 Access Point (AP) mode?<br>
If yes then how-to used physical push button in ESP32 Access Point (AP) mode.<br>
 I have two Scenarios  :<br>
1. First push button used as physical as well as  using web server.<br>
2. Second pushbutton used only physically, but its state(on/off) shown on  web server.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=530465#respond" data-commentid="530465" data-postid="67766" data-belowelement="div-comment-530465" data-respondelement="respond" data-replyto="Reply to Asad Shaikh" aria-label="Reply to Asad Shaikh">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-530562" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2">
			<article id="div-comment-530562" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-530562">
								<time datetime="2020-12-18T10:50:48+00:00" itemprop="datePublished">
									December 18, 2020 at 10:50 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
You can do all of that in access point mode.<br>
Take a look at these tutorials that might help:<br>
<a href="https://randomnerdtutorials.com/esp32-websocket-server-arduino/" rel="nofollow ugc">https://randomnerdtutorials.com/esp32-websocket-server-arduino/</a><br>
<a href="https://randomnerdtutorials.com/esp32-esp8266-web-server-physical-button/" rel="nofollow ugc">https://randomnerdtutorials.com/esp32-esp8266-web-server-physical-button/</a><br>
<a href="https://randomnerdtutorials.com/esp32-esp8266-web-server-outputs-momentary-switch/" rel="nofollow ugc">https://randomnerdtutorials.com/esp32-esp8266-web-server-outputs-momentary-switch/</a><br>
Then, just modify the code to use access point.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=530562#respond" data-commentid="530562" data-postid="67766" data-belowelement="div-comment-530562" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-533222" class="comment even thread-even depth-1">
			<article id="div-comment-533222" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/42a79ee11e0aef82e44cf6ff52db80cd.png" srcset="https://secure.gravatar.com/avatar/42a79ee11e0aef82e44cf6ff52db80cd?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Christian Reder</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-533222">
								<time datetime="2020-12-25T15:10:48+00:00" itemprop="datePublished">
									December 25, 2020 at 3:10 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi,<br>
i would like to set up an ESP32 Access Point with an IP address other than 192.168.4.1 .<br>
IPAddress IP = WiFi.softAPIP(); always gives the same IP.<br>
Is there a way to do that?<br>
Thx<br>
Christian</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=533222#respond" data-commentid="533222" data-postid="67766" data-belowelement="div-comment-533222" data-respondelement="respond" data-replyto="Reply to Christian Reder" aria-label="Reply to Christian Reder">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-536038" class="comment odd alt thread-odd thread-alt depth-1 parent">
			<article id="div-comment-536038" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/750e4f97e1492c0756efdc7689d46cf1.png" srcset="https://secure.gravatar.com/avatar/750e4f97e1492c0756efdc7689d46cf1?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Victor Das Neves</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-536038">
								<time datetime="2021-01-02T15:49:35+00:00" itemprop="datePublished">
									January 2, 2021 at 3:49 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi,<br>
When I attempt to compile the code provided for “Setting the ESP32 as an Access Point”, I get the following error</p>
<p>‘class WiFiClass’ has no member named ‘softAP’</p>
<p>highlighting the following line<br>
WiFi.softAP(ssid, password);</p>
<p>I have looked in my directories and there is no WiFi.h which has this function it it.<br>
Can you assist.<br>
Thank you<br>
Victor</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=536038#respond" data-commentid="536038" data-postid="67766" data-belowelement="div-comment-536038" data-respondelement="respond" data-replyto="Reply to Victor Das Neves" aria-label="Reply to Victor Das Neves">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-536376" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-536376" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-536376">
								<time datetime="2021-01-03T11:56:17+00:00" itemprop="datePublished">
									January 3, 2021 at 11:56 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Victor.<br>
Make sure you have an ESP32 board selected when you try to compile and upload the code.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=536376#respond" data-commentid="536376" data-postid="67766" data-belowelement="div-comment-536376" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-543435" class="comment odd alt thread-even depth-1 parent">
			<article id="div-comment-543435" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/73e117e5b301dd86060a332098f0abb0.png" srcset="https://secure.gravatar.com/avatar/73e117e5b301dd86060a332098f0abb0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Jonathan Miller</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-543435">
								<time datetime="2021-01-20T20:38:48+00:00" itemprop="datePublished">
									January 20, 2021 at 8:38 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hello, and thank you for the awesome tutorials.</p>
<p>For my project I am hoping to have two separate ESP32s (clients/stations) both reading data from magnetometer sensors wired to them, and have them both send the data live to a third ESP32 (server/AP). Maybe I am missing something, but the code reads as if as soon as it is connected to a single client, it won’t look for new clients anymore. How can I connect several clients to an ESP32 server and communicate simultaneously?</p>
<p>thank you!</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=543435#respond" data-commentid="543435" data-postid="67766" data-belowelement="div-comment-543435" data-respondelement="respond" data-replyto="Reply to Jonathan Miller" aria-label="Reply to Jonathan Miller">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-544810" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-544810" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-544810">
								<time datetime="2021-01-23T11:46:46+00:00" itemprop="datePublished">
									January 23, 2021 at 11:46 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
Have you taken a look at ESP-NOW or ESP-MESH. These are probably a better alternative for your project:<br>
<a href="https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/" rel="nofollow ugc">https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/</a><br>
<a href="https://randomnerdtutorials.com/esp-mesh-esp32-esp8266-painlessmesh/" rel="nofollow ugc">https://randomnerdtutorials.com/esp-mesh-esp32-esp8266-painlessmesh/</a><br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=544810#respond" data-commentid="544810" data-postid="67766" data-belowelement="div-comment-544810" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-543965" class="comment odd alt thread-odd thread-alt depth-1">
			<article id="div-comment-543965" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/73e117e5b301dd86060a332098f0abb0.png" srcset="https://secure.gravatar.com/avatar/73e117e5b301dd86060a332098f0abb0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn"><a href="http://none/" rel="external nofollow ugc" class="url">Jonathan Miller</a></cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-543965">
								<time datetime="2021-01-21T17:27:02+00:00" itemprop="datePublished">
									January 21, 2021 at 5:27 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hello,</p>
<p>I left a comment here yesterday but I don’t see it posted. Does it take a while for the comment to be posted or did mine just fail to go through?</p>
<p>I’m asking about connecting multiple ESP32 clients to a single ESP32 server simultaneously as I don’t see how the code allows for that even though the guide seems to hint that multiple clients is possible. In the code it seems as though as soon as a new client is detected the server will no longer look for new clients. Can you help me with this?</p>
<p>Thank you very much for the great guides and for your response!</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=543965#respond" data-commentid="543965" data-postid="67766" data-belowelement="div-comment-543965" data-respondelement="respond" data-replyto="Reply to Jonathan Miller" aria-label="Reply to Jonathan Miller">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-551866" class="comment even thread-even depth-1 parent">
			<article id="div-comment-551866" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/167e6fbb948f9ab6cb369219ba17eba8.png" srcset="https://secure.gravatar.com/avatar/167e6fbb948f9ab6cb369219ba17eba8?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Steve</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-551866">
								<time datetime="2021-02-07T20:25:35+00:00" itemprop="datePublished">
									February 7, 2021 at 8:25 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>The next logical step after this would be to enable mDNS so the user could connect via known name instead of needing the printed IP address.  For an ESP32 this is as easy as:</p>
<p>#include &lt;ESPmDNS.h&gt;</p>
<p>In setup add:<br>
if (!MDNS.begin(“esp32lights”)) {<br>
   Serial.println(“Error setting up MDNS responder!”);<br>
   while (1) {<br>
      delay(1000);<br>
    }<br>
}<br>
Serial.println(“MDNS started.”);<br>
MDNS.addService(“http”, “tcp”, 80);</p>
<p>If you’re connecting from a Windows PC you’d have to install the Apple Bonjour service, but from anything else you could connect to the ESP32 access point and simply browse to<br>
<a href="http://esp32lights.local/" rel="nofollow ugc">http://esp32lights.local</a></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=551866#respond" data-commentid="551866" data-postid="67766" data-belowelement="div-comment-551866" data-respondelement="respond" data-replyto="Reply to Steve" aria-label="Reply to Steve">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-553044" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2">
			<article id="div-comment-553044" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-553044">
								<time datetime="2021-02-09T12:20:38+00:00" itemprop="datePublished">
									February 9, 2021 at 12:20 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Thanks for sharing.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=553044#respond" data-commentid="553044" data-postid="67766" data-belowelement="div-comment-553044" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-562437" class="comment even thread-odd thread-alt depth-1 parent">
			<article id="div-comment-562437" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/d094fee3f885afdbebdba0397288b26d.png" srcset="https://secure.gravatar.com/avatar/d094fee3f885afdbebdba0397288b26d?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">PAULO SERGIO LOPES</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-562437">
								<time datetime="2021-02-25T14:40:27+00:00" itemprop="datePublished">
									February 25, 2021 at 2:40 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>hello!<br>
Tanks for the article first of all!<br>
I need to undestand if I can change the IP Adress to another by my will<br>
for example 192.168.0.1</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=562437#respond" data-commentid="562437" data-postid="67766" data-belowelement="div-comment-562437" data-respondelement="respond" data-replyto="Reply to PAULO SERGIO LOPES" aria-label="Reply to PAULO SERGIO LOPES">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-562533" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2">
			<article id="div-comment-562533" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-562533">
								<time datetime="2021-02-25T18:31:18+00:00" itemprop="datePublished">
									February 25, 2021 at 6:31 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
Yes, if it is available in your local network.<br>
Regards,<br>
Sar</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=562533#respond" data-commentid="562533" data-postid="67766" data-belowelement="div-comment-562533" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-575759" class="comment even thread-even depth-1">
			<article id="div-comment-575759" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/0b7b3f243d8287e2523f3f91fcdc856e.png" srcset="https://secure.gravatar.com/avatar/0b7b3f243d8287e2523f3f91fcdc856e?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Liam T Donovan</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-575759">
								<time datetime="2021-03-21T21:31:54+00:00" itemprop="datePublished">
									March 21, 2021 at 9:31 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi,</p>
<p>When I use this on my ESP32, it automatically logs me into my Wifi, even though I didn’t go to the access point and gave it my credentials. How is this possible.</p>
<p>Another question I have is, if a network that is scanned doesn’t require a password, with the esp32 automatically connect to that network?</p>
<p>Thanks</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=575759#respond" data-commentid="575759" data-postid="67766" data-belowelement="div-comment-575759" data-respondelement="respond" data-replyto="Reply to Liam T Donovan" aria-label="Reply to Liam T Donovan">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-588120" class="comment odd alt thread-odd thread-alt depth-1">
			<article id="div-comment-588120" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/6e6ca06f1e5e8c81e2818d0e41863948.png" srcset="https://secure.gravatar.com/avatar/6e6ca06f1e5e8c81e2818d0e41863948?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Pratik</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-588120">
								<time datetime="2021-04-11T11:24:01+00:00" itemprop="datePublished">
									April 11, 2021 at 11:24 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>I am getting this error while connecting to the wifi, though the wifi is connected but cant get to the web page.</p>
<p>Setting AP (Access Point)…AP IP address: 192.168.4.1<br>
E (36263) event: mismatch or invalid event, id=63<br>
E (36263) event: default event handler failed!<br>
dhcps: send_offer&gt;&gt;udp_sendto result 0</p>
<p>help.<br>
Thanks</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=588120#respond" data-commentid="588120" data-postid="67766" data-belowelement="div-comment-588120" data-respondelement="respond" data-replyto="Reply to Pratik" aria-label="Reply to Pratik">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-588130" class="comment even thread-even depth-1 parent">
			<article id="div-comment-588130" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/6e6ca06f1e5e8c81e2818d0e41863948.png" srcset="https://secure.gravatar.com/avatar/6e6ca06f1e5e8c81e2818d0e41863948?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Pratik</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-588130">
								<time datetime="2021-04-11T11:31:53+00:00" itemprop="datePublished">
									April 11, 2021 at 11:31 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>I just found that I am able connect through my windows 10 pc but not through my android phone.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=588130#respond" data-commentid="588130" data-postid="67766" data-belowelement="div-comment-588130" data-respondelement="respond" data-replyto="Reply to Pratik" aria-label="Reply to Pratik">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-588726" class="comment byuser comment-author-sara-santos bypostauthor odd alt depth-2">
			<article id="div-comment-588726" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-588726">
								<time datetime="2021-04-12T09:17:44+00:00" itemprop="datePublished">
									April 12, 2021 at 9:17 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
You need to make sure that your phone connects to the ESP32 wi-fi network.<br>
regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=588726#respond" data-commentid="588726" data-postid="67766" data-belowelement="div-comment-588726" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-602711" class="comment even thread-odd thread-alt depth-1 parent">
			<article id="div-comment-602711" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/3e659c554a44763f59f849c30a7f2383.png" srcset="https://secure.gravatar.com/avatar/3e659c554a44763f59f849c30a7f2383?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Gabriel Bachur</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-602711">
								<time datetime="2021-05-07T13:43:06+00:00" itemprop="datePublished">
									May 7, 2021 at 1:43 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi, Sara.</p>
<p>I need some help.. The IDE has been showing this Error message:</p>
<p>=================================================================</p>
<p>error: ‘class WiFiClass’ has no member named ‘softAPIP’</p>
<p>Serial.println(WiFi.softAPIP()); //imprime o IP do AP</p>
<p>=================================================================<br>
I’ve already checked the board i’m using (“ESP32 Dev Module”)<br>
I’ve already reinstalled the libraries<br>
I tried to declare the libraries with ” ” and put them in the same directory of the file .ino<br>
Nothing worked! Can you help to understand what is going wrong?? And how can i fix it?</p>
<p>Thanks</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=602711#respond" data-commentid="602711" data-postid="67766" data-belowelement="div-comment-602711" data-respondelement="respond" data-replyto="Reply to Gabriel Bachur" aria-label="Reply to Gabriel Bachur">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-603369" class="comment odd alt depth-2 parent">
			<article id="div-comment-603369" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/167e6fbb948f9ab6cb369219ba17eba8.png" srcset="https://secure.gravatar.com/avatar/167e6fbb948f9ab6cb369219ba17eba8?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Steve Prior</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-603369">
								<time datetime="2021-05-08T16:14:17+00:00" itemprop="datePublished">
									May 8, 2021 at 4:14 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Remove the (), it’s a constant not a function.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=603369#respond" data-commentid="603369" data-postid="67766" data-belowelement="div-comment-603369" data-respondelement="respond" data-replyto="Reply to Steve Prior" aria-label="Reply to Steve Prior">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-603477" class="comment even depth-3">
			<article id="div-comment-603477" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/167e6fbb948f9ab6cb369219ba17eba8.png" srcset="https://secure.gravatar.com/avatar/167e6fbb948f9ab6cb369219ba17eba8?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Steve Prior</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-603477">
								<time datetime="2021-05-08T20:42:37+00:00" itemprop="datePublished">
									May 8, 2021 at 8:42 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Ignore my comment, I was incorrect working from memory.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=603477#respond" data-commentid="603477" data-postid="67766" data-belowelement="div-comment-603477" data-respondelement="respond" data-replyto="Reply to Steve Prior" aria-label="Reply to Steve Prior">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-604784" class="comment odd alt thread-even depth-1 parent">
			<article id="div-comment-604784" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/fe2862e1d0364cce0916919b1b412e39.png" srcset="https://secure.gravatar.com/avatar/fe2862e1d0364cce0916919b1b412e39?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Ali</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-604784">
								<time datetime="2021-05-11T19:38:19+00:00" itemprop="datePublished">
									May 11, 2021 at 7:38 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi sara,<br>
As I understand it, when we call  “softAP()”  method , esp32 establishes an access point<br>
So how can i remove this access point?<br>
Can i destroy this access point created by esp32 by calling the “begin()” method?</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=604784#respond" data-commentid="604784" data-postid="67766" data-belowelement="div-comment-604784" data-respondelement="respond" data-replyto="Reply to Ali" aria-label="Reply to Ali">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-605020" class="comment byuser comment-author-sara-santos bypostauthor even depth-2">
			<article id="div-comment-605020" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-605020">
								<time datetime="2021-05-12T10:49:19+00:00" itemprop="datePublished">
									May 12, 2021 at 10:49 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
Set the mode to WiFi.mode(WIFI_STA) to set it to station.<br>
Learn more here: <a href="https://randomnerdtutorials.com/esp32-useful-wi-fi-functions-arduino/#1" rel="nofollow ugc">https://randomnerdtutorials.com/esp32-useful-wi-fi-functions-arduino/#1</a><br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=605020#respond" data-commentid="605020" data-postid="67766" data-belowelement="div-comment-605020" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

		<li id="comment-606813" class="comment odd alt thread-odd thread-alt depth-1 parent">
			<article id="div-comment-606813" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/c7fefffc1c01977ece36d8e0d77dacb6.jpeg" srcset="https://secure.gravatar.com/avatar/c7fefffc1c01977ece36d8e0d77dacb6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Mark</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-606813">
								<time datetime="2021-05-15T17:54:19+00:00" itemprop="datePublished">
									May 15, 2021 at 5:54 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>“Open your web browser and type the IP address 192.168.4.1. The web server page should load:”</p>
<p>Nope. Even though I can connect to the AP, and the serial monitor says 192.168.4.1 is the IP address, attempts to access that IP through the browser indicate that the page is not reachable.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=606813#respond" data-commentid="606813" data-postid="67766" data-belowelement="div-comment-606813" data-respondelement="respond" data-replyto="Reply to Mark" aria-label="Reply to Mark">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-606948" class="comment byuser comment-author-sara-santos bypostauthor even depth-2 parent">
			<article id="div-comment-606948" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/25e3da92f25bc3fde695d9c0d92207b0.png" srcset="https://secure.gravatar.com/avatar/25e3da92f25bc3fde695d9c0d92207b0?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Sara Santos</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-606948">
								<time datetime="2021-05-15T22:18:36+00:00" itemprop="datePublished">
									May 15, 2021 at 10:18 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi.<br>
In your device network settings (computer or smartphone, depends on where you want to access your web server), you need to connect to the ESP32 access point before typing the IP on the browser.<br>
Regards,<br>
Sara</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=606948#respond" data-commentid="606948" data-postid="67766" data-belowelement="div-comment-606948" data-respondelement="respond" data-replyto="Reply to Sara Santos" aria-label="Reply to Sara Santos">Reply</a></span>				</div>
			</article>
			<ul class="children">

		<li id="comment-606960" class="comment odd alt depth-3">
			<article id="div-comment-606960" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/c7fefffc1c01977ece36d8e0d77dacb6.jpeg" srcset="https://secure.gravatar.com/avatar/c7fefffc1c01977ece36d8e0d77dacb6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Mark</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-606960">
								<time datetime="2021-05-15T23:02:31+00:00" itemprop="datePublished">
									May 15, 2021 at 11:02 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Yes. As I mentioned, I did connect to the AP successfully. I just can’t access the page in the browser.</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=606960#respond" data-commentid="606960" data-postid="67766" data-belowelement="div-comment-606960" data-respondelement="respond" data-replyto="Reply to Mark" aria-label="Reply to Mark">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-606978" class="comment even depth-3">
			<article id="div-comment-606978" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/c7fefffc1c01977ece36d8e0d77dacb6.jpeg" srcset="https://secure.gravatar.com/avatar/c7fefffc1c01977ece36d8e0d77dacb6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Mark</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-606978">
								<time datetime="2021-05-15T23:35:01+00:00" itemprop="datePublished">
									May 15, 2021 at 11:35 pm								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>But I appreciate the article! It is a great starting point. I’ll figure out the issue. It just didn’t work right off like I’d hoped. <img draggable="false" role="img" class="emoji" alt="🙂" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/1f642.svg"></p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=606978#respond" data-commentid="606978" data-postid="67766" data-belowelement="div-comment-606978" data-respondelement="respond" data-replyto="Reply to Mark" aria-label="Reply to Mark">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->

		<li id="comment-607003" class="comment odd alt depth-3">
			<article id="div-comment-607003" class="comment-body" itemtype="https://schema.org/Comment" itemscope="">
				<footer class="comment-meta" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
					<img alt="" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/c7fefffc1c01977ece36d8e0d77dacb6.jpeg" srcset="https://secure.gravatar.com/avatar/c7fefffc1c01977ece36d8e0d77dacb6?s=100&amp;d=mm&amp;r=g 2x" class="avatar avatar-50 photo" height="50" width="50" loading="lazy">					<div class="comment-author-info">
						<div class="comment-author vcard" itemprop="author" itemtype="https://schema.org/Person" itemscope="">
							<cite itemprop="name" class="fn">Mark</cite>						</div>

						<div class="entry-meta comment-metadata">
							<a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/#comment-607003">
								<time datetime="2021-05-16T01:00:08+00:00" itemprop="datePublished">
									May 16, 2021 at 1:00 am								</time>
							</a>
													</div>
					</div>

									</footer>

				<div class="comment-content" itemprop="text">
					<p>Hi Sara – It does work in the loop() as it turns out. I’m trying to put the loop into a FreeRTOS task where I need it to be, but not successful yet. I’ll figure it out… thanks!</p>
<span class="reply"><a rel="nofollow" class="comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?replytocom=607003#respond" data-commentid="607003" data-postid="67766" data-belowelement="div-comment-607003" data-respondelement="respond" data-replyto="Reply to Mark" aria-label="Reply to Mark">Reply</a></span>				</div>
			</article>
			</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->
		</ol><!-- .comment-list -->

			<div id="respond" class="comment-respond">
		<h3 id="reply-title" class="comment-reply-title">Leave a Comment <small><a rel="nofollow" id="cancel-comment-reply-link" href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/?fbclid=IwAR0Ea3EVlbVWnRkcigocR1lGoeJPR_inBQCiIHF8UK2jHLJOUO1dtQuKMtk#respond" style="display:none;">Cancel reply</a></small></h3><form action="https://randomnerdtutorials.com/wp-comments-post.php" method="post" id="commentform" class="comment-form" novalidate=""><p class="comment-form-comment"><label for="comment" class="screen-reader-text">Comment</label><textarea id="comment" name="comment" cols="45" rows="8" aria-required="true" required=""></textarea></p><label for="author" class="screen-reader-text">Name</label><input placeholder="Name *" id="author" name="author" type="text" value="" size="30">
<label for="email" class="screen-reader-text">Email</label><input placeholder="Email *" id="email" name="email" type="email" value="" size="30">
<label for="url" class="screen-reader-text">Website</label><input placeholder="Website" id="url" name="url" type="url" value="" size="30">
<p class="comment-subscription-form"><input type="checkbox" name="subscribe_comments" id="subscribe_comments" value="subscribe" style="width: auto; -moz-appearance: checkbox; -webkit-appearance: checkbox;"> <label class="subscribe-label" id="subscribe-label" for="subscribe_comments">Notify me of follow-up comments by email.</label></p><p class="comment-subscription-form"><input type="checkbox" name="subscribe_blog" id="subscribe_blog" value="subscribe" style="width: auto; -moz-appearance: checkbox; -webkit-appearance: checkbox;"> <label class="subscribe-label" id="subscribe-blog-label" for="subscribe_blog">Notify me of new posts by email.</label></p><p class="form-submit"><input name="submit" type="submit" id="submit" class="submit" value="Post Comment"> <input type="hidden" name="comment_post_ID" value="67766" id="comment_post_ID">
<input type="hidden" name="comment_parent" id="comment_parent" value="0">
</p><p style="display: none;"><input type="hidden" id="akismet_comment_nonce" name="akismet_comment_nonce" value="be587c6666"></p><textarea name="ak_hp_textarea" cols="45" rows="8" maxlength="100" style="display: none !important;"></textarea><input type="hidden" id="ak_js" name="ak_js" value="1628258131434"></form>	</div><!-- #respond -->
	
</div><!-- #comments -->
			</div>

					</main>
	</div>

	<div id="left-sidebar" class="widget-area sidebar is-left-sidebar grid-15 tablet-grid-15 mobile-grid-100 grid-parent pull-60 tablet-pull-60" itemtype="https://schema.org/WPSideBar" itemscope="">
	<div class="inside-left-sidebar">
		<aside id="text-54" class="widget inner-padding widget_text">			<div class="textwidget"><div class="rnt-sb-m">
<p><span class="rnt-shl">Learn ESP32</span></p>
<p><a href="https://randomnerdtutorials.com/getting-started-with-esp32/">ESP32 Introduction</a></p>
<p><a href="https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/">ESP32 Arduino IDE</a></p>
<p><a href="https://randomnerdtutorials.com/installing-esp32-arduino-ide-2-0/">ESP32 Arduino IDE 2.0</a></p>
<p><a href="https://randomnerdtutorials.com/vs-code-platformio-ide-esp32-esp8266-arduino/">VS Code and PlatformIO</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-pinout-reference-gpios/">ESP32 Pinout</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-digital-inputs-outputs-arduino/">ESP32 Inputs Outputs</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-pwm-arduino-ide/">ESP32 PWM</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-adc-analog-read-arduino-ide/">ESP32 Analog Inputs</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-pir-motion-sensor-interrupts-timers/">ESP32 Interrupts Timers</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-deep-sleep-arduino-ide-wake-up-sources/">ESP32 Deep Sleep</a></p>
<p><span class="rnt-shl">Protocols</span></p>
<p><a href="https://randomnerdtutorials.com/esp32-web-server-arduino-ide/">ESP32 Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-lora-rfm95-transceiver-arduino-ide/">ESP32 LoRa</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-bluetooth-low-energy-ble-arduino-ide/">ESP32 BLE</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-bluetooth-classic-arduino-ide/">ESP32 Bluetooth</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-mqtt-publish-subscribe-arduino-ide/">ESP32 MQTT</a></p>
<p><a href="https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/">ESP32 ESP-NOW</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-client-server-wi-fi/">ESP32 Wi-Fi</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-websocket-server-arduino/">ESP32 WebSocket</a></p>
<p><a href="https://randomnerdtutorials.com/esp-mesh-esp32-esp8266-painlessmesh/">ESP32 ESP-MESH</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-send-email-smtp-server-arduino-ide/">ESP32 Email</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-sim800l-send-text-messages-sms/">ESP32 Text Messages</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-http-get-post-arduino/">ESP32 HTTP GET POST</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-http-get-open-weather-map-thingspeak-arduino/">HTTP GET Web APIs</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-http-post-ifttt-thingspeak-arduino/">HTTP POST Web APIs</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-web-server-sent-events-sse/">Server-Sent Events</a></p>
<p><span class="rnt-shl">Web Servers</span></p>
<p><a href="https://randomnerdtutorials.com/esp32-web-server-arduino-ide/">Output Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-web-server-slider-pwm/">PWM Slider Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-web-server-websocket-sliders/">PWM Multiple Sliders Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-async-web-server-espasyncwebserver-library/">Async Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-relay-module-ac-web-server/">Relay Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-servo-motor-web-server-arduino-ide/">Servo Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-dht11-dht22-temperature-humidity-web-server-arduino-ide/">DHT Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-web-server-with-bme280-mini-weather-station/">BME280 Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-bme680-web-server-arduino/">BME680 Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-ds18b20-temperature-arduino-ide/">DS18B20 Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-lora-sensor-web-server/">LoRa Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-plot-chart-web-server/">Plot/Chart Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-plot-readings-charts-multiple/">Chart Multiple Series Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-web-server-spiffs-spi-flash-file-system/">SPIFFS Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-thermostat-web-server/">Thermostat Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-web-server-outputs-momentary-switch/">Momentary Switch Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-web-server-physical-button/">Physical Button Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-input-data-html-form/">Input Fields Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/display-images-esp32-esp8266-web-server/">Images Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-rgb-led-strip-web-server/">RGB LED Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-web-server-timer-pulse/">Timer/Pulse Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-web-server-http-authentication/">HTTP Auth Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-mpu-6050-web-server/">MPU-6050 Web Server</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-web-server-microsd-card/">MicroSD Card Web Server</a></p>
<p><span class="rnt-shl">DIY Cloud</span></p>
<p><a href="https://randomnerdtutorials.com/cloud-weather-station-esp32-esp8266/">ESP32 Weather Station</a></p>
<p><a href="https://randomnerdtutorials.com/control-esp32-esp8266-gpios-from-anywhere/">Control GPIOs</a></p>
<p><a href="https://randomnerdtutorials.com/visualize-esp32-esp8266-sensor-readings-from-anywhere/">View Sensor Readings</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-mysql-database-php/">ESP32 MySQL</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-send-email-notification/">ESP32 PHP Email</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-sim800l-publish-data-to-cloud/">ESP32 SIM800L</a></p>
<p><a href="https://randomnerdtutorials.com/access-node-red-dashboard-anywhere-digital-ocean/">Cloud Node-RED Dashboard</a></p>
<p><a href="https://randomnerdtutorials.com/cloud-mqtt-mosquitto-broker-access-anywhere-digital-ocean/">Cloud MQTT Broker</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-cloud-mqtt-broker-sim800l/">ESP32 Cloud MQTT</a></p>
<p><span class="rnt-shl">ESP-NOW</span></p>
<p><a href="https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/">ESP-NOW Introduction</a></p>
<p><a href="https://randomnerdtutorials.com/esp-now-two-way-communication-esp32/">ESP-NOW Two-Way</a></p>
<p><a href="https://randomnerdtutorials.com/esp-now-one-to-many-esp32-esp8266/">ESP-NOW One-to-Many</a></p>
<p><a href="https://randomnerdtutorials.com/esp-now-many-to-one-esp32/">ESP-NOW Many-to-One</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp-now-wi-fi-web-server/">ESP-NOW + Wi-Fi Web Server</a></p>
<p><span class="rnt-shl">Modules</span></p>
<p><a href="https://randomnerdtutorials.com/esp32-relay-module-ac-web-server/">ESP32 Relay Module</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-dc-motor-l298n-motor-driver-control-speed-direction/">ESP32 DC Motors</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-servo-motor-web-server-arduino-ide/">ESP32 Servo</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-microsd-card-arduino/">ESP32 MicroSD Card</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-data-logging-temperature-to-microsd-card/">ESP32 MicroSD Card Data Logging</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-pir-motion-sensor-interrupts-timers/">ESP32 PIR</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-hc-sr04-ultrasonic-arduino/">ESP32 HC-SR04</a></p>
<p><span class="rnt-shl">Sensors</span></p>
<p><a href="https://randomnerdtutorials.com/esp32-dht11-dht22-temperature-humidity-sensor-arduino-ide/">ESP32 DHT11/DHT22</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-bme280-arduino-ide-pressure-temperature-humidity/">ESP32 BME280</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-bme680-sensor-arduino/">ESP32 BME680</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-ds18b20-temperature-arduino-ide/">ESP32 DS18B20</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-multiple-ds18b20-temperature-sensors/">ESP32 Multiple DS18B20</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-with-bmp180-barometric-sensor/">ESP32 BMP180</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-bmp388-arduino/">ESP32 BMP388</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-mqtt-publish-dht11-dht22-arduino/">MQTT DHT11/DHT22</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-mqtt-publish-bme280-arduino/">MQTT BME280</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-mqtt-publish-bme680-arduino/">MQTT BME680</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-mqtt-publish-ds18b20-temperature-arduino/">MQTT DS18B20</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-mpu-6050-accelerometer-gyroscope-arduino/">ESP32 MPU-6050</a></p>
<p><span class="rnt-shl">Displays</span></p>
<p><a href="https://randomnerdtutorials.com/esp32-ssd1306-oled-display-arduino-ide/">ESP32 OLED</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-i2c-lcd-arduino-ide/">ESP32 LCD</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-dht-temperature-and-humidity-oled-display/">OLED Temperature</a></p>
<p><span class="rnt-shl">ESP32 Features</span></p>
<p><a href="https://randomnerdtutorials.com/esp32-hall-effect-sensor/">ESP32 Hall Sensor</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-touch-pins-arduino-ide/">ESP32 Touch Sensor</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-i2c-communication-arduino-ide/">ESP32 I2C</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-flash-memory/">ESP32 Flash Memory</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-dual-core-arduino-ide/">ESP32 Dual Core</a></p>
<p><span class="rnt-shl">Useful Guides</span></p>
<p><a href="https://randomnerdtutorials.com/esp32-troubleshooting-guide/">ESP32 Troubleshooting</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-access-point-ap-web-server/">ESP32 Access Point</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-static-fixed-ip-address-arduino-ide/">ESP32 Fixed IP Address</a></p>
<p><a href="https://randomnerdtutorials.com/get-change-esp32-esp8266-mac-address-arduino/">ESP32 MAC Address</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-set-custom-hostname-arduino/">ESP32 Hostname</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-over-the-air-ota-programming/">ESP32 OTA</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-ota-over-the-air-arduino/">ESP32 OTA Arduino</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-ota-over-the-air-vs-code/">ESP32 OTA VS Code</a></p>
<p><a href="https://randomnerdtutorials.com/power-esp32-esp8266-solar-panels-battery-level-monitoring/">ESP32 Solar Panels</a></p>
<p><a href="https://randomnerdtutorials.com/alexa-echo-with-esp32-and-esp8266/">ESP32 Alexa</a></p>
<p><a href="https://randomnerdtutorials.com/install-esp32-filesystem-uploader-arduino-ide/">ESP32 Install SPIFFS</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-date-time-ntp-client-server-arduino/">ESP32 Time and Date</a></p>
<p><a href="https://randomnerdtutorials.com/epoch-unix-time-esp32-arduino/">ESP32 Epoch Time</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-esp8266-publish-sensor-readings-to-google-sheets/">ESP32 Google Sheets</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-email-alert-temperature-threshold/">ESP32 Email Altert</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-thingspeak-publish-arduino/">ESP32 ThingSpeak</a></p>
<p><a href="https://randomnerdtutorials.com/build-an-all-in-one-esp32-weather-station-shield/">Weather Station Shield</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-iot-shield-pcb-dashboard/">ESP32 IoT Shield</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-weather-station-pcb/">ESP32 Weather Station PCB</a></p>
<p><a href="https://randomnerdtutorials.com/vs-code-platformio-ide-esp32-esp8266-arduino/">VS Code and PlatformIO</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-vs-code-platformio-spiffs/">VS Code SPIFFS</a></p>
<p><a href="https://randomnerdtutorials.com/vs-code-workspaces-esp32-esp8266/">VS Code Workspaces</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-save-data-permanently-preferences/">Save Data Preferences Library</a></p>
<p><a href="https://randomnerdtutorials.com/solved-reconnect-esp32-to-wifi/">Reconnect to Wi-Fi</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-useful-wi-fi-functions-arduino/">Useful Wi-Fi Functions</a></p>
<p><span class="rnt-shl">Other Projects</span></p>
<p><a href="https://randomnerdtutorials.com/telegram-control-esp32-esp8266-nodemcu-outputs/">Telegram Control Outputs</a></p>
<p><a href="https://randomnerdtutorials.com/telegram-request-esp32-esp8266-nodemcu-sensor-readings/">Telegram Sensor Readings</a></p>
<p><a href="https://randomnerdtutorials.com/telegram-esp32-motion-detection-arduino/">Telegram Detect Motion</a></p>
<p><a href="https://randomnerdtutorials.com/telegram-group-esp32-esp8266/">Telegram Group</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-status-indicator-sensor-pcb/">ESP32 Status PCB</a></p>
<p><a href="https://randomnerdtutorials.com/altimeter-datalogger-esp32-bmp388/">ESP32 BMP388 Datalogger</a></p>
<p><span class="rnt-shl">ESP32 Boards</span></p>
<p><a href="https://randomnerdtutorials.com/esp32-cam-video-streaming-face-recognition-arduino-ide/">ESP32 Camera</a></p>
<p><a href="https://randomnerdtutorials.com/ttgo-lora32-sx1276-arduino-ide/">ESP32 LoRa</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-built-in-oled-ssd1306/">ESP32 OLED</a></p>
<p><a href="https://randomnerdtutorials.com/esp32-sim800l-send-text-messages-sms/">ESP32 SIM800L</a></p>
<p><span class="rnt-shl">Learn More</span></p>
<p><a href="https://randomnerdtutorials.com/projects-esp32/">Learn ESP32</a></p>
<p><a href="https://randomnerdtutorials.com/projects-esp8266/">Learn ESP8266</a></p>
<p><a href="https://randomnerdtutorials.com/projects-esp32-cam/">Learn ESP32-CAM</a></p>
<p><a href="https://randomnerdtutorials.com/projects-esp32-esp8266-micropython/">Learn MicroPython</a></p>
<p><a href="https://randomnerdtutorials.com/projects-arduino/">Learn Arduino</a></p>
<p><a href="https://randomnerdtutorials.com/build-web-servers-esp32-esp8266-ebook/"><strong>Build Web Servers eBook</strong></a></p>
<p><a href="https://randomnerdtutorials.com/learn-esp32-with-arduino-ide/"><strong>ESP32 Premium Course »</strong></a></p>
</div>
</div>
		</aside><aside id="search-4" class="widget inner-padding widget_search"><form method="get" class="search-form" action="https://randomnerdtutorials.com/">
	<label>
		<span class="screen-reader-text">Search for:</span>
		<input type="search" class="search-field" placeholder="Search …" value="" name="s" title="Search for:">
	</label>
	<input type="submit" class="search-submit" value="Search"></form>
</aside>	</div>
</div>
<div id="right-sidebar" class="widget-area sidebar is-right-sidebar grid-25 tablet-grid-25 grid-parent" itemtype="https://schema.org/WPSideBar" itemscope="">
	<div class="inside-right-sidebar">
		<aside id="text-49" class="widget inner-padding widget_text">			<div class="textwidget"><p><a href="https://makeradvisor.com/?utm_source=rnt&amp;utm_medium=sb&amp;utm_campaign=sb" target="_blank" rel="noopener"><img class="aligncenter" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/lab-sb-img.jpg" loading="lazy" width="341" height="192"></a><br>
<strong><a href="https://makeradvisor.com/?utm_source=rnt&amp;utm_medium=sb&amp;utm_campaign=sb" target="_blank" rel="noopener">Visit Maker Advisor – Tools and Gear for makers, hobbyists and DIYers »</a></strong></p>
</div>
		</aside><aside id="text-47" class="widget inner-padding widget_text">			<div class="textwidget"><p><a href="https://randomnerdtutorials.com/home-automation-using-esp8266/"><img class="aligncenter" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/esp8266-sb-img(1).jpg" loading="lazy" width="341" height="192"></a><br>
<strong><a href="https://randomnerdtutorials.com/home-automation-using-esp8266/">Home Automation using ESP8266 eBook and video course »</a> </strong>Build IoT and home automation projects.</p>
</div>
		</aside><aside id="text-46" class="widget inner-padding widget_text">			<div class="textwidget"><p><a href="https://randomnerdtutorials.com/build-a-home-automation-system-for-100/"><img class="aligncenter" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/home-automation-sb-img(1).jpg" loading="lazy" width="341" height="192"></a><br>
<strong><a href="https://randomnerdtutorials.com/build-a-home-automation-system-for-100/">Build a Home Automation System from Scratch »</a>&nbsp;</strong>With Raspberry Pi, ESP8266, Arduino, and Node-RED.</p>
</div>
		</aside>	</div>
</div>

	</div>
</div>


<div class="site-footer footer-bar-active footer-bar-align-center">
			<footer class="site-info" itemtype="https://schema.org/WPFooter" itemscope="" style="content-visibility:auto;contain-intrinsic-size:1px 1000px;">
			<div class="inside-site-info grid-container grid-parent">
						<div class="footer-bar">
			<aside id="nav_menu-10" class="widget inner-padding widget_nav_menu"><div class="menu-footer-disclaimer-container"><ul id="menu-footer-disclaimer" class="menu"><li id="menu-item-82503" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-82503"><a href="https://randomnerdtutorials.com/about/">About</a></li>
<li id="menu-item-20492" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20492"><a href="https://randomnerdtutorials.com/support">Support</a></li>
<li id="menu-item-20493" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20493"><a href="https://randomnerdtutorials.com/terms">Terms and Conditions</a></li>
<li id="menu-item-20495" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20495"><a href="https://randomnerdtutorials.com/privacy-policy/">Privacy Policy</a></li>
<li id="menu-item-20494" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20494"><a href="https://randomnerdtutorials.com/returns-and-refunds/">Refunds</a></li>
<li id="menu-item-103055" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-103055"><a target="_blank" rel="noreferrer noopener nofollow" href="https://www.livroreclamacoes.pt/inicio/">Complaints’ Book</a></li>
<li id="menu-item-43625" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-43625"><a target="_blank" rel="noopener" href="https://makeradvisor.com/">MakerAdvisor.com</a></li>
<li id="menu-item-20496" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-20496"><a target="_blank" rel="noopener" href="https://rntlab.com/">Join the Lab</a></li>
</ul></div></aside>		</div>
						<div class="copyright-bar">
					Copyright © 2013-2021 · RandomNerdTutorials.com · All Rights Reserved				</div>
			</div>
		</footer>
		</div>

		
		<link rel="stylesheet" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.23.0/themes/prism.min.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/prism.min.css">
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/prism.min.js.download" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/prism-c.min.js.download" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/prism-python.min.js.download" defer=""></script>
<link rel="stylesheet" id="elementor-post-83032-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/0374b13add6b.post-83032.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/0374b13add6b.post-83032.css">
<link rel="stylesheet" id="elementor-post-82533-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/32493e4e071e.post-82533.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/32493e4e071e.post-82533.css">
<link rel="stylesheet" id="elementor-post-82829-css" media="all" data-lazy-method="interaction" data-lazy-attributes="href" data-lazy-href="https://randomnerdtutorials.com/wp-content/cache/flying-press/randomnerdtutorials.com/34c8bc3901e5.post-82829.css" href="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/34c8bc3901e5.post-82829.css">
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/sticky.min.js.download" id="generate-sticky-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/photon.min.js.download" id="jetpack-photon-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/preload.min.js.download" id="flying_press_preload-js" defer=""></script>
<!--[if lte IE 11]>
<script src='https://randomnerdtutorials.com/wp-content/themes/generatepress/assets/js/classList.min.js?ver=3.0.3' id='generate-classlist-js'></script>
<![endif]-->
<script id="generate-main-js-extra">
var generatepressMenu = {"toggleOpenedSubMenus":"1","openSubMenuLabel":"Open Sub-Menu","closeSubMenuLabel":"Close Sub-Menu"};
</script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/main.min.js.download" id="generate-main-js" defer=""></script>
<script id="generate-navigation-search-js-extra">
var generatepressNavSearch = {"open":"Open Search Bar","close":"Close Search Bar"};
</script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/navigation-search.min.js.download" id="generate-navigation-search-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/comment-reply.min.js.download" id="comment-reply-js"></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/wp-embed.min.js.download" id="wp-embed-js"></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/imagesloaded.min.js.download" id="imagesloaded-js"></script>
<script async="async" src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/270f0cd7341b.form.js.download" id="akismet-form-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/webpack-pro.runtime.min.js.download" id="elementor-pro-webpack-runtime-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/webpack.runtime.min.js.download" id="elementor-webpack-runtime-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/frontend-modules.min.js.download" id="elementor-frontend-modules-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/jquery.sticky.min.js.download" id="elementor-sticky-js" defer=""></script>
<script id="elementor-pro-frontend-js-before">
var ElementorProFrontendConfig = {"ajaxurl":"https:\/\/randomnerdtutorials.com\/wp-admin\/admin-ajax.php","nonce":"87abffe691","urls":{"assets":"https:\/\/randomnerdtutorials.com\/wp-content\/plugins\/elementor-pro\/assets\/"},"i18n":{"toc_no_headings_found":"No headings were found on this page."},"shareButtonsNetworks":{"facebook":{"title":"Facebook","has_counter":true},"twitter":{"title":"Twitter"},"google":{"title":"Google+","has_counter":true},"linkedin":{"title":"LinkedIn","has_counter":true},"pinterest":{"title":"Pinterest","has_counter":true},"reddit":{"title":"Reddit","has_counter":true},"vk":{"title":"VK","has_counter":true},"odnoklassniki":{"title":"OK","has_counter":true},"tumblr":{"title":"Tumblr"},"digg":{"title":"Digg"},"skype":{"title":"Skype"},"stumbleupon":{"title":"StumbleUpon","has_counter":true},"mix":{"title":"Mix"},"telegram":{"title":"Telegram"},"pocket":{"title":"Pocket","has_counter":true},"xing":{"title":"XING","has_counter":true},"whatsapp":{"title":"WhatsApp"},"email":{"title":"Email"},"print":{"title":"Print"}},"facebook_sdk":{"lang":"en_US","app_id":""},"lottie":{"defaultAnimationUrl":"https:\/\/randomnerdtutorials.com\/wp-content\/plugins\/elementor-pro\/modules\/lottie\/assets\/animations\/default.json"}};
</script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/frontend.min.js.download" id="elementor-pro-frontend-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/waypoints.min.js.download" id="elementor-waypoints-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/core.min.js.download" id="jquery-ui-core-js"></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/swiper.min.js.download" id="swiper-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/share-link.min.js.download" id="share-link-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/dialog.min.js.download" id="elementor-dialog-js" defer=""></script>
<script id="elementor-frontend-js-before">
var elementorFrontendConfig = {"environmentMode":{"edit":false,"wpPreview":false,"isScriptDebug":false},"i18n":{"shareOnFacebook":"Share on Facebook","shareOnTwitter":"Share on Twitter","pinIt":"Pin it","download":"Download","downloadImage":"Download image","fullscreen":"Fullscreen","zoom":"Zoom","share":"Share","playVideo":"Play Video","previous":"Previous","next":"Next","close":"Close"},"is_rtl":false,"breakpoints":{"xs":0,"sm":480,"md":768,"lg":1025,"xl":1440,"xxl":1600},"responsive":{"breakpoints":{"mobile":{"label":"Mobile","value":767,"direction":"max","is_enabled":true},"mobile_extra":{"label":"Mobile Extra","value":880,"direction":"max","is_enabled":false},"tablet":{"label":"Tablet","value":1024,"direction":"max","is_enabled":true},"tablet_extra":{"label":"Tablet Extra","value":1365,"direction":"max","is_enabled":false},"laptop":{"label":"Laptop","value":1620,"direction":"max","is_enabled":false},"widescreen":{"label":"Widescreen","value":2400,"direction":"min","is_enabled":false}}},"version":"3.2.5","is_static":false,"experimentalFeatures":{"form-submissions":true,"video-playlist":true},"urls":{"assets":"https:\/\/randomnerdtutorials.com\/wp-content\/plugins\/elementor\/assets\/"},"settings":{"page":[],"editorPreferences":[]},"kit":{"active_breakpoints":["viewport_mobile","viewport_tablet"],"lightbox_enable_counter":"yes","lightbox_enable_fullscreen":"yes","lightbox_enable_zoom":"yes","lightbox_enable_share":"yes","lightbox_title_src":"title","lightbox_description_src":"description"},"post":{"id":67766,"title":"ESP32%20Access%20Point%20%28AP%29%20for%20Web%20Server%20%7C%20Random%20Nerd%20Tutorials","excerpt":"","featuredImage":"https:\/\/i0.wp.com\/randomnerdtutorials.com\/wp-content\/uploads\/2018\/07\/ESP32-access-point-1.jpg?fit=828%2C466&quality=100&strip=all&ssl=1"}};
</script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/frontend.min.js(1).download" id="elementor-frontend-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/preloaded-elements-handlers.min.js.download" id="pro-preloaded-elements-handlers-js" defer=""></script>
<script src="./ESP32 Access Point (AP) for Web Server _ Random Nerd Tutorials_files/preloaded-modules.min.js.download" id="preloaded-modules-js" defer=""></script>

<script>const loadElemsOnUserInteraction=function(){const t=["mouseover","keydown","touchstart","touchmove","wheel"],e=function e(){n(),clearTimeout(o),t.forEach(function(t){window.removeEventListener(t,e,{passive:!0})})};var n=function(){document.querySelectorAll("[data-lazy-method='interaction']").forEach(function(t){t.getAttribute("data-lazy-attributes").split(",").forEach(function(e){const n=t.getAttribute("data-lazy-".concat(e));t.setAttribute(e,n)})})},o=setTimeout(e,10e3);t.forEach(function(t){window.addEventListener(t,e,{passive:!0})})};loadElemsOnUserInteraction();const loadElemsOnViewPort=function(){var t=new IntersectionObserver(function(e){e.forEach(function(e){if(e.isIntersecting){t.unobserve(e.target),e.target.getAttribute("data-lazy-attributes").split(",").forEach(function(t){const n=e.target.getAttribute("data-lazy-".concat(t));e.target.setAttribute(t,n)})}})},{rootMargin:"300px"});document.querySelectorAll("[data-lazy-method='viewport']").forEach(function(e){t.observe(e)})};loadElemsOnViewPort();</script>
<span id="elementor-device-mode" class="elementor-screen-only"></span><script>mendeleyWebImporter = {
  downloadPdfs(t,e) { return this._call('downloadPdfs', [t,e]); },
  open() { return this._call('open', []); },
  setLoginToken(t) { return this._call('setLoginToken', [t]); },
  _call(methodName, methodArgs) {
    const id = Math.random();
    window.postMessage({ id, token: '0.008089011156960257', methodName, methodArgs }, 'https://randomnerdtutorials.com');
    return new Promise(resolve => {
      const listener = window.addEventListener('message', event => {
        const data = event.data;
        if (typeof data !== 'object' || !('result' in data) || data.id !== id) return;
        window.removeEventListener('message', listener);
        resolve(data.result);
      });
    });
  }
};</script><div class="dialog-widget dialog-lightbox-widget dialog-type-buttons dialog-type-lightbox elementor-popup-modal" id="elementor-popup-modal-83058" style="display: none;"><div class="dialog-widget-content dialog-lightbox-widget-content animated"><div class="dialog-header dialog-lightbox-header"></div><div class="dialog-message dialog-lightbox-message"></div><div class="dialog-buttons-wrapper dialog-lightbox-buttons-wrapper"></div></div><div class="dialog-close-button dialog-lightbox-close-button"><i class="eicon-close"></i></div></div></body><grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration></html>
