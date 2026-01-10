<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="glass-header q-py-sm" height-hint="98">
      <q-toolbar>
        <q-toolbar-title
          class="text-weight-bold row items-center cursor-pointer"
          @click="$router.push('/')"
        >
          <div class="logo-container q-mr-sm">
            <q-icon name="dashboard" color="white" size="28px" />
          </div>
          <span class="text-white text-h5" style="letter-spacing: 1px"
            >CMS<span class="text-primary text-italic">PRO</span></span
          >
        </q-toolbar-title>

        <q-space />

        <div class="q-gutter-md row items-center no-wrap gt-sm">
          <a href="#" class="nav-link">Home</a>
          <a href="#" class="nav-link">Features</a>
          <a href="#" class="nav-link">Solutions</a>
          <a href="#" class="nav-link">Pricing</a>

          <q-separator vertical color="grey-8" class="q-mx-md" />

          <q-btn flat class="nav-btn-login" label="Log In" no-caps />
          <q-btn
            unelevated
            class="nav-btn-signup"
            label="Get Started"
            no-caps
            icon-right="arrow_forward"
          />
        </div>

        <q-btn flat dense round icon="menu" aria-label="Menu" class="lt-md" />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="bg-black text-white q-py-lg">
      <div class="row justify-center q-gutter-md">
        <div class="text-caption text-grey">© 2026 CMS Pro. All rights reserved.</div>
      </div>
    </q-footer>
  </q-layout>
</template>

<script setup>
// Layout logic here
</script>

<style scoped>
.glass-header {
  background: rgba(10, 10, 10, 0.7);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
  transition: all 0.3s ease;
}

.logo-container {
  background: linear-gradient(135deg, #d32f2f 0%, #aa0000 100%);
  padding: 6px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 15px rgba(211, 47, 47, 0.4);
}

.nav-link {
  color: #a0a0a0;
  text-decoration: none;
  font-weight: 500;
  font-size: 15px;
  position: relative;
  transition: color 0.3s ease;
  padding: 5px 0;
}

.nav-link:hover {
  color: #ffffff;
}

.nav-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: 0px;
  left: 0;
  background-color: #d32f2f;
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

.nav-btn-login {
  color: white;
  font-weight: 600;
  transition: color 0.3s;
}

.nav-btn-login:hover {
  color: #d32f2f;
  background: transparent;
}

.nav-btn-signup {
  background: #d32f2f;
  color: white;
  font-weight: 600;
  border-radius: 8px;
  padding: 8px 20px;
  transition:
    transform 0.2s,
    box-shadow 0.2s;
}

.nav-btn-signup:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(211, 47, 47, 0.4);
  background: #b71c1c;
}
</style>
