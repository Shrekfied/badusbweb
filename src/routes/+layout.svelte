<svelte:head>
   <link rel="stylesheet" href="style.css">
   <title>USBPi Control Panel</title>
</svelte:head>

<script>
   import titleStore from "$lib/stores/titleStore";

   let title;

   titleStore.subscribe(value => {
      title = value;
   });
</script>

<div id="wrapper" class="site-navigation-resize">
   <div id="container" class=" clearfix">
      <div id="sidebar-left" class="sidebar ">
         <div id="content-left-top">
            <div class="profile-picture-wrapper">
               <div class="profile-picture">
                  <img src="logo.png" alt="USBPi Logo" title="">
               </div>
            </div>
         </div>
         
         <div id="left-nav" role="navigation">
            <div id="menu-s-home" role="navigation"></div>
            <div id="menu-s-main">
               <ul class="menu" role="menu">
                  <li role="menuitem" class="expanded first active-trail odd">
                     <div class="link-wrapper menu-235 course-profile-left-menu active-trail-dist-2">
                        <a href="/course/2603759481" class="course-profile-left-menu" role="menuitem">
                        <span>
                        <span class="visually-hidden">Current Menu Item</span>
                        </span>Course Profile </a>
                     </div>
                     <ul class="menu" role="menu">
                        <li role="menuitem" class="collapsed first active-trail even">
                           <div class="link-wrapper materials-icon active-trail-dist-1">
                              <a href="/terminal" class="materials-icon active" role="menuitem">
                              <span>
                              <span class="visually-hidden">Current Menu Item</span>
                              </span>Terminal
                              </a>
                           </div>
                        </li>
                        <li role="menuitem" class="leaf odd">
                           <div class="link-wrapper attendance-icon">
                              <a href="/files" class="attendance-icon" role="menuitem">
                              <span></span>File Browser</a>
                           </div>
                        </li>
                        <li role="menuitem" class="leaf odd">
                           <div class="link-wrapper menu-1025 updates-icon">
                              <a href="/devices" class="menu-1025 updates-icon" role="menuitem">
                              <span></span>USB Devices </a>
                           </div>
                        </li>
                        <li role="menuitem" class="leaf odd">
                           <div class="link-wrapper updates-icon">
                              <a href="/storage" class="menu-1025 updates-icon" role="menuitem">
                              <span></span>USB Storage </a>
                           </div>
                        </li>
                        <li role="menuitem" class="leaf last even">
                           <div class="link-wrapper menu-821 members-icon">
                              <a href="/ducky" class="members-icon" role="menuitem">
                              <span></span>Rubber Ducky </a>
                           </div>
                        </li>
                        <li role="menuitem" class="leaf even">
                           <div class="link-wrapper grades-icon">
                              <a href="/pihole" class="grades-icon" role="menuitem">
                              <span></span>Network Blocking </a>
                           </div>
                        </li>
                        <li role="menuitem" class="leaf odd">
                           <div class="link-wrapper attendance-icon">
                              <a href="/dns" class="attendance-icon" role="menuitem">
                              <span></span>DNS Server </a>
                           </div>
                        </li>
                        <li role="menuitem" class="leaf odd">
                           <div class="link-wrapper attendance-icon">
                              <a href="/vpn" class="attendance-icon" role="menuitem">
                              <span></span>VPN Configuration </a>
                           </div>
                        </li>
                        <li role="menuitem" class="leaf odd">
                           <div class="link-wrapper menu-557 members-icon">
                              <a href="/router" class="menu-557 members-icon" role="menuitem">
                              <span></span>Wi-Fi Access Point </a>
                           </div>
                        </li>
                        <li role="menuitem" class="leaf odd">
                           <div class="link-wrapper menu-557 attendance-icon">
                              <a href="/about" class="menu-557 attendance-icon" role="menuitem">
                              <span></span>About</a>
                           </div>
                        </li>
                     </ul>
                  </li>
                  <li role="menuitem" class="collapsed last even">
                     <div class="link-wrapper menu-4027 course-profile-left-menu">
                        <a href="/course-templates/2603759481" class="menu-4027 course-profile-left-menu" role="menuitem">
                        <span></span>Course Profile </a>
                     </div>
                  </li>
               </ul>
            </div>
         </div>
         <div id="content-left">
            <div class="left-block-wrapper">
               <h3 class="h3-med-flat">Statistics</h3>
               <div class="left-block">
                  <div class="course-info-wrapper">
                     <p class="course-info"></p>
                     <dl>
                        <dt>CPU Usage</dt>
                        <dd>30%</dd>
                        <dt>Memory Usage</dt>
                        <dd>53mb / 437mb</dd>
                        <dt>Storage</dt>
                        <dd>6.2gb / 15.7gb</dd>
                        <dt>Uptime</dt>
                        <dd>0.37 Hours</dd>
                     </dl>
                  </div>
               </div>
            </div>
         </div>
      </div>

      <div id="main-content-wrapper" class="clearfix ">
         <div id="center-wrapper" class="">
            <div id="center-inner" class="clearfix">
               <div id="center-top">
                  <h1 class="page-title ">
                     <span>USBPi Control Panel</span>
                  </h1>
                  <h2>
                     <span>{title}</span>
                  </h2>
                  <div class="content-top">
                     <div class="content-top-wrapper">
                        <div class="realm-top-right">
                              <button class="button">Reboot</button>
                        </div>
                     </div>
                  </div>
               </div>
               <div id="content-wrapper">
                  <div id="center">
                     <div id="main">
                        <div id="main-inner">
                           <div class="s-js-course-materials-full course-materials-full" id="course-profile-materials">
                              <div class="materials-top"></div>
                              <div class="full-view s-js-materials-body s-js-full-view" id="course-profile-materials-folders">
                                 <slot />
                              </div>
                           </div>
                        </div>
                     </div>
                  </div>
               </div>
            </div>
         </div>
         <!-- /#center-wrapper -->
      </div>
      <!-- /#main-content-wrapper -->
   </div>
   <!-- /#container -->
   <div id="footer" class="clearfix " role="contentinfo"></div>
   <span class="clear clearfix bottom-span"></span>
</div>