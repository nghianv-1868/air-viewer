<template>
  <header class="header-global">
    <base-nav class="navbar-main" transparent type="" effect="light" expand>
      <nuxt-link slot="brand" class="navbar-brand mr-lg-5" :to="$i18n.path('')">
        <img src="/argon/img/brand/white.png" alt="logo">
      </nuxt-link>

      <div slot="content-header" slot-scope="{closeMenu}" class="row">
        <div class="col-6 collapse-brand">
          <nuxt-link :to="$i18n.path('')">
            <img src="/argon/img/brand/blue.png">
          </nuxt-link>
        </div>
        <div class="col-6 collapse-close">
          <close-button @click="closeMenu" />
        </div>
      </div>

      <!-- <ul class="navbar-nav navbar-nav-hover align-items-lg-center">
        <base-dropdown class="nav-item" menu-classes="dropdown-menu-xl">
          <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
            <i class="ni ni-ui-04 d-lg-none" />
            <span class="nav-link-inner--text">Explore</span>
          </a>
          <div class="dropdown-menu-inner">
            <a
              href="https://demos.creative-tim.com/vue-argon-design-system/documentation/"
              class="media d-flex align-items-center"
            >
              <div class="icon icon-shape bg-gradient-primary rounded-circle text-white">
                <i class="ni ni-spaceship" />
              </div>
              <div class="media-body ml-3">
                <h6 class="heading text-primary mb-md-1">Getting started</h6>
                <p class="description d-none d-md-inline-block mb-0">Get started with Bootstrap, the
                  world's most popular framework for building responsive sites.</p>
              </div>
            </a>
            <a
              href="https://demos.creative-tim.com/vue-argon-design-system/documentation/"
              class="media d-flex align-items-center"
            >
              <div class="icon icon-shape bg-gradient-warning rounded-circle text-white">
                <i class="ni ni-ui-04" />
              </div>
              <div class="media-body ml-3">
                <h5 class="heading text-warning mb-md-1">Components</h5>
                <p class="description d-none d-md-inline-block mb-0">Learn how to use Argon
                  compiling Scss, change brand colors and more.</p>
              </div>
            </a>
          </div>
        </base-dropdown>
      </ul> -->
      <ul class="navbar-nav align-items-lg-center ml-lg-auto">
        <li class="nav-item">
          <nuxt-link
            class="nav-link nav-link-icon mt-1"
            :to="$i18n.path('faq')"
            rel="noopener"
            data-toggle="tooltip"
            :title="$t('navbar.faqs.title')"
          >
            <i class="fa fa-question-circle" />
            <span class="nav-link-inner--text d-lg-none">{{ $t('navbar.faqs.title') }}</span>
          </nuxt-link>
        </li>
        <li class="nav-item">
          <a
            class="nav-link nav-link-icon"
            href="https://www.facebook.com/SunAsteriskVietnam"
            target="_blank"
            rel="noopener"
            data-toggle="tooltip"
            :title="$t('navbar.facebook.title')"
          >
            <i class="fab fa-facebook-square" />
            <span class="nav-link-inner--text d-lg-none">{{ $t('navbar.facebook.title') }}</span>
          </a>
        </li>
        <li class="nav-item">
          <a
            class="nav-link nav-link-icon"
            href="https://github.com/sun-asterisk-research/air-visual"
            target="_blank"
            rel="noopener"
            data-toggle="tooltip"
            :title="$t('navbar.github.title')"
          >
            <i class="fab fa-github" />
            <span class="nav-link-inner--text d-lg-none">{{ $t('navbar.github.title') }}</span>
          </a>
        </li>
        <li class="nav-item">
          <nuxt-link
            v-if="$i18n.locale === 'en'"
            :to="`/vi` + $route.fullPath"
            class="nav-link"
            active-class="none"
            exact
          >
            <span class="nav-link-inner--text">{{ $t('links.vietnamese') }}</span>
          </nuxt-link>
          <nuxt-link
            v-else
            :to="$route.fullPath.replace(/^\/[^\/]+/, '')"
            class="nav-link"
            active-class="none"
            exact
          >
            <span class="nav-link-inner--text">{{ $t('links.english') }}</span>
          </nuxt-link>
        </li>
        <!-- <base-dropdown v-if="isAuthenticated" tag="li" class="nav-item d-md-block ml-lg-4">
          <a slot="title" href="#" class="nav-link btn btn-neutral btn-icon" data-toggle="dropdown" role="button">
            <i class="ni ni-collection d-lg-none" />
            <span class="nav-link-inner--text text-color">{{ loggedInUser }}</span>
          </a>
          <a class="dropdown-item cursor" @click="logout">
            <i class="ni ni-user-run" />
            Logout
          </a>
        </base-dropdown>
        <li v-else class="nav-item d-lg-block ml-lg-4">
          <nuxt-link to="/login" class="btn btn-neutral btn-icon">
            <span class="btn-inner--icon">
              <i class="fa fa-cloud-download mr-2" />
            </span>
            <span class="nav-link-inner--text">Login</span>
          </nuxt-link>
        </li> -->
      </ul>
    </base-nav>
  </header>
</template>
<script>
import { mapGetters } from 'vuex'
import BaseNav from '~/components/argon/BaseNav'
import BaseDropdown from '~/components/argon/BaseDropdown'
import CloseButton from '~/components/argon/CloseButton'

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown
  }
}
</script>
<style type="scss">
.text-color {
  color:black;
}

.cursor {
  cursor: pointer;
}
</style>
