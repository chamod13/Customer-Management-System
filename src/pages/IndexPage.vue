<template>
  <q-page class="bg-dark text-white">
    <!-- Hero Section -->
    <section class="hero-section row items-center q-pa-md q-py-xl" style="min-height: 85vh">
      <div class="container row items-center q-mx-auto q-col-gutter-xl">
        <!-- Left Content: Text -->
        <div class="col-12 col-md-6 text-left q-gutter-md">
          <div class="reveal-fade-up">
            <q-badge color="primary" label="NEW: AI-POWERED INSIGHTS" class="q-mb-md" rounded />
            <h1 class="text-h2 text-weight-bold q-my-none text-white leading-tight">
              Master Your <br /><span class="text-primary">Customer Relationships</span>
            </h1>
            <p class="text-h5 text-grey-4 q-my-md" style="max-width: 600px; line-height: 1.5">
              The ultimate platform to manage, analyze, and grow your customer base with intelligent
              automation and real-time data.
            </p>
          </div>

          <div class="row justify-start q-gutter-md q-pt-md reveal-fade-up delay-100">
            <q-btn
              size="lg"
              color="primary"
              label="Get Started Free"
              no-caps
              class="q-px-xl shadow-10"
              rounded
            />
            <q-btn
              size="lg"
              outline
              color="white"
              label="Watch Demo"
              icon="play_circle"
              no-caps
              class="q-px-xl"
              rounded
            />
          </div>

          <!-- Trust Indicators -->
          <div
            class="q-mt-xl pt-5 row justify-start items-center q-gutter-lg opacity-70 reveal-fade-up delay-200"
          >
            <div class="text-caption text-grey">TRUSTED BY TEAMS AT</div>
            <q-icon name="business" size="sm" color="grey" />
            <q-icon name="store" size="sm" color="grey" />
            <q-icon name="domain" size="sm" color="grey" />
          </div>
        </div>

        <!-- Right Content: Image -->
        <div class="col-12 col-md-6 text-center relative-position">
          <div class="hero-image-container floating-animation">
            <div class="glow-effect"></div>
            <img
              src="~assets/hero-dashboard.png"
              alt="CMS Dashboard"
              class="responsive-image glass-panel"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="bg-black q-py-xl border-top-red">
      <div class="row justify-evenly text-center container q-mx-auto">
        <div class="col-12 col-md-3 q-pa-md">
          <div class="text-h3 text-primary text-weight-bold">10k+</div>
          <div class="text-subtitle1 text-grey">Active Users</div>
        </div>
        <div class="col-12 col-md-3 q-pa-md">
          <div class="text-h3 text-primary text-weight-bold">99%</div>
          <div class="text-subtitle1 text-grey">Satisfaction Rate</div>
        </div>
        <div class="col-12 col-md-3 q-pa-md">
          <div class="text-h3 text-primary text-weight-bold">24/7</div>
          <div class="text-subtitle1 text-grey">AI Support</div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="q-py-xl q-px-md bg-dark-page">
      <div class="text-center q-mb-xl">
        <h2 class="text-h3 text-weight-bold">Powerful Features</h2>
        <p class="text-grey text-h6">Everything you need to scale your business</p>
      </div>

      <div class="row q-col-gutter-lg container q-mx-auto">
        <div class="col-12 col-md-4" v-for="(feature, index) in features" :key="index">
          <q-card class="bg-grey-10 text-white no-shadow border-gray q-pa-lg hover-effect h-100">
            <q-card-section>
              <q-avatar
                color="primary"
                text-color="white"
                :icon="feature.icon"
                size="60px"
                class="q-mb-md"
              />
              <div class="text-h5 text-weight-bold q-mb-sm">{{ feature.title }}</div>
              <div class="text-grey-4">{{ feature.dsec }}</div>
            </q-card-section>
          </q-card>
        </div>
      </div>
    </section>

    <!-- App Preview / Detailed Feature -->
    <section class="q-py-xl q-px-md">
      <div class="row items-center container q-mx-auto q-col-gutter-xl">
        <div class="col-12 col-md-6 order-last order-md-first">
          <q-card
            class="bg-gray-10 no-shadow"
            style="border-radius: 20px; border: 1px solid #333; overflow: hidden"
          >
            <!-- Placeholder for an app screenshot or complex UI visualization -->
            <div
              class="bg-grey-9 q-pa-xl text-center"
              style="height: 300px; display: flex; align-items: center; justify-content: center"
            >
              <q-icon name="dashboard" size="100px" color="grey-8" />
              <div class="text-h6 text-grey-6 q-mt-md">Interactive Dashboard Preview</div>
            </div>
          </q-card>
        </div>
        <div class="col-12 col-md-6">
          <h3 class="text-h3 text-weight-bold q-mb-md">
            Manage Customers <br /><span class="text-primary">Like a Pro</span>
          </h3>
          <p class="text-grey-4 text-h6 q-mb-lg">
            Our intuitive dashboard gives you a bird's-eye view of your sales pipeline, customer
            interactions, and team performance.
          </p>
          <q-list dark padding>
            <q-item>
              <q-item-section avatar><q-icon name="check_circle" color="primary" /></q-item-section>
              <q-item-section>Real-time activity tracking</q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar><q-icon name="check_circle" color="primary" /></q-item-section>
              <q-item-section>Automated follow-ups</q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar><q-icon name="check_circle" color="primary" /></q-item-section>
              <q-item-section>Detailed customer profiles</q-item-section>
            </q-item>
          </q-list>
          <q-btn outline color="white" label="Learn More" class="q-mt-lg" rounded />
        </div>
      </div>
    </section>

    <!-- Call to Action -->
    <section class="bg-primary text-white q-py-xl text-center">
      <h2 class="text-h3 text-weight-bold q-mb-md">Ready to grow your business?</h2>
      <p class="text-h6 q-mb-xl opacity-80">Join thousands of companies using our CMS today.</p>
      <q-btn
        color="white"
        text-color="primary"
        size="lg"
        label="Start Your Free Trial"
        rounded
        class="text-weight-bold"
      />
    </section>
  </q-page>
</template>

<script setup>
const features = [
  {
    title: 'Smart Analytics',
    dsec: 'Get detailed insights into customer behavior and sales trends with our AI-powered analytics engine.',
    icon: 'analytics',
  },
  {
    title: 'Seamless Automation',
    dsec: 'Automate repetitive tasks and focus on what matters most - building relationships with your customers.',
    icon: 'auto_mode',
  },
  {
    title: 'Secure Database',
    dsec: 'Keep your customer data safe with enterprise-grade security and automatic cloud backups.',
    icon: 'security',
  },
  {
    title: 'Team Collaboration',
    dsec: 'Share notes, assign tasks, and track performance across your entire sales team in real-time.',
    icon: 'groups',
  },
  {
    title: 'Multi-Channel Support',
    dsec: 'Connect with customers via Email, SMS, and Social Media directly from a single dashboard.',
    icon: 'hub',
  },
  {
    title: 'Custom Reports',
    dsec: 'Generate beautiful, branded reports to share with stakeholders and track your KPIs.',
    icon: 'summarize',
  },
]
</script>

<style scoped>
.hero-section {
  background: radial-gradient(circle at top right, #330000 0%, #000000 60%);
  overflow: hidden;
}

.border-top-red {
  border-top: 2px solid #d32f2f;
}

.bg-dark-page {
  background-color: #0e0e0e;
}

.border-gray {
  border: 1px solid #1f1f1f;
}

.hover-effect {
  transition:
    transform 0.3s ease,
    border-color 0.3s ease;
}

.hover-effect:hover {
  transform: translateY(-5px);
  border-color: #d32f2f;
}

.container {
  max-width: 1200px;
}

/* New Hero Styles */
.leading-tight {
  line-height: 1.1;
}

.responsive-image {
  max-width: 100%;
  height: auto;
  border-radius: 20px;
}

.glass-panel {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
}

.hero-image-container {
  position: relative;
  z-index: 10;
}

.glow-effect {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 80%;
  height: 80%;
  background: radial-gradient(circle, rgba(211, 47, 47, 0.3) 0%, rgba(0, 0, 0, 0) 70%);
  z-index: -1;
  filter: blur(50px);
}

/* Animations */
.floating-animation {
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-20px);
  }
  100% {
    transform: translateY(0px);
  }
}

.reveal-fade-up {
  opacity: 0;
  transform: translateY(30px);
  animation: fadeUp 0.8s ease-out forwards;
}

.delay-100 {
  animation-delay: 0.1s;
}
.delay-200 {
  animation-delay: 0.2s;
}

@keyframes fadeUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
