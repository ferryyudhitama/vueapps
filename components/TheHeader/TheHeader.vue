<template>
<header  class="fixed-top">
  <b-navbar toggleable="md" type="dark" variant="info">

        <b-container>

            <b-navbar-brand href="#" left>Logo</b-navbar-brand>

            <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

            <b-collapse is-nav id="nav_collapse">
            
                <!-- Right aligned nav items -->
                <b-navbar-nav class="ml-auto">

                <b-navbar-nav right>
                    <b-nav-item href="#">Inspiration</b-nav-item>
                    <b-nav-item href="#">Membership </b-nav-item>
                    <b-nav-item href="#">Spa & Wellbeing  </b-nav-item>
                    <b-nav-item href="#">News & Events</b-nav-item>
                    <b-nav-item href="#">Contact Us</b-nav-item>
                
                </b-navbar-nav>

            
                </b-navbar-nav>

            </b-collapse>
        </b-container>
    </b-navbar>
</header>

</template>

<style scoped>
.bg-info {
    background-color: #000000!important;
}
.navbar-dark .navbar-nav .nav-link {
    color: #fff;
    font-size: 1.1rem;
    margin-right: 10px;
    font-weight: 500;
}

.navbar-dark .navbar-nav .nav-link:hover{
   color:  #8d714c;

}

@media screen and (max-width: 770px) {
    .navbar-nav {
        text-align: center;
        padding-top: 10px;
    }   
}
</style>