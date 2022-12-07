<template>
  <nord-navigation slot="nav">
    <nord-dropdown slot="header" expand>
      <nord-button class="n-logo" slot="toggle" expand variant="switch">
        <!-- This doesn’t use avatar component since we want it to be editable in theme editor -->
        <div slot="start" aria-hidden="true" class="n-clinic-img"></div>
        <span slot="start" aria-hidden="true" class="n-clinic-icon"
          ><span>B</span></span
        >
        <span class="n-clinic-name">Bath Clinic</span>
      </nord-button>
      <nord-dropdown-group heading="laura.williams@nordhealth.com">
        <nord-dropdown-item>
          <nord-avatar slot="start" name="Bath Clinic" size="s" variant="square"
            >B</nord-avatar
          >
          Bath Clinic
          <nord-icon slot="end" name="interface-checked" size="s"></nord-icon>
        </nord-dropdown-item>
        <nord-dropdown-item>
          <nord-avatar
            slot="start"
            name="Ocean Beach Clinic"
            size="s"
            variant="square"
            style="--n-avatar-color: var(--n-color-status-success)"
          >
            O
          </nord-avatar>
          Ocean Beach Clinic
        </nord-dropdown-item>
        <nord-dropdown-item>
          <nord-avatar
            slot="start"
            name="Park Animal Hospital"
            size="s"
            variant="square"
            style="--n-avatar-color: var(--n-color-status-highlight)"
          >
            P
          </nord-avatar>
          Park Animal Hospital
        </nord-dropdown-item>
        <nord-dropdown-item>
          <nord-avatar
            slot="start"
            name="Balboa Pet Hospital"
            size="s"
            variant="square"
            style="--n-avatar-color: var(--n-color-status-danger)"
          >
            B
          </nord-avatar>
          Balboa Pet Hospital
        </nord-dropdown-item>
      </nord-dropdown-group>
      <nord-dropdown-group>
        <nord-dropdown-item>Add another clinic</nord-dropdown-item>
        <nord-dropdown-item>Customize style</nord-dropdown-item>
      </nord-dropdown-group>
      <nord-dropdown-item>Sign out from all clinics</nord-dropdown-item>
    </nord-dropdown>

    <nord-nav-group>
      <nord-nav-item aria-describedby="search" icon="navigation-search"
        >Search</nord-nav-item
      >
      <nord-tooltip id="search" position="inline-end">
        Search
        <div slot="shortcut">
          <nord-icon
            name="keyboard-option"
            size="s"
            label="Option key"
          ></nord-icon>
        </div>
        <span slot="shortcut">S</span>
      </nord-tooltip>
      <nord-nav-item
        icon="navigation-notifications"
        aria-describedby="notifications"
        badge="12"
      >
        Notifications
      </nord-nav-item>
      <nord-tooltip id="notifications" position="inline-end">
        Notifications
        <div slot="shortcut">
          <nord-icon
            name="keyboard-option"
            size="s"
            label="Option key"
          ></nord-icon>
        </div>
        <span slot="shortcut">N</span>
      </nord-tooltip>
      <nord-nav-item icon="navigation-tasks" aria-describedby="tasks"
        >My tasks</nord-nav-item
      >
      <nord-tooltip id="tasks" position="inline-end">
        My tasks
        <div slot="shortcut">
          <nord-icon
            name="keyboard-option"
            size="s"
            label="Option key"
          ></nord-icon>
        </div>
        <span slot="shortcut">M</span>
      </nord-tooltip>
    </nord-nav-group>
    <nord-nav-group heading="Workspace">
      <NuxtLink to="/" custom>
        <template #default="{ navigate, href, isActive }">
          <nord-nav-item
            icon="navigation-dashboard"
            :href="href"
            @click="navigate"
            :active="isActive || null"
            >Dashboard</nord-nav-item
          >
        </template>
      </NuxtLink>
      <nord-nav-item icon="navigation-payments">
        Payments
        <nord-nav-group slot="subnav">
          <nord-nav-item href="#">All transactions</nord-nav-item>
          <nord-nav-item href="#">Payments</nord-nav-item>
          <nord-nav-item href="#">Disputes</nord-nav-item>
        </nord-nav-group>
      </nord-nav-item>
      <nord-nav-item icon="navigation-reports">
        Reports
        <nord-nav-group slot="subnav">
          <nord-nav-item href="#">Payments</nord-nav-item>
          <nord-nav-item href="#">Disputes</nord-nav-item>
          <nord-nav-item href="#">Payouts</nord-nav-item>
        </nord-nav-group>
      </nord-nav-item>
      <NuxtLink to="/settings" custom>
        <template #default="{ navigate, href, isActive }">
          <nord-nav-item
            icon="navigation-settings"
            :href="href"
            @click="navigate"
            :active="isActive || null"
            >Settings</nord-nav-item
          >
        </template>
      </NuxtLink>
    </nord-nav-group>

    <nord-select
      :label="$t('language')"
      v-model="$i18n.locale"
      class="n-margin-bs-m"
      expand
    >
      <option value="en">English</option>
      <option value="fr">French</option>
      <option value="he">Hebrew</option>
    </nord-select>

    <nord-dropdown expand slot="footer">
      <nord-button class="account-button" slot="toggle" expand variant="plain">
        <nord-avatar
          aria-hidden="true"
          name="Laura Williams"
          slot="start"
        ></nord-avatar>
        <nord-icon
          slot="end"
          name="interface-dropdown-small"
          size="s"
        ></nord-icon>
        Laura Williams
      </nord-button>
      <nord-dropdown-group>
        <nord-dropdown-item href="#">View profile</nord-dropdown-item>
        <nord-dropdown-item>Settings</nord-dropdown-item>
      </nord-dropdown-group>
      <nord-dropdown-group>
        <nord-dropdown-item>
          Show keyboard shortcuts
          <div slot="end" class="n-color-text-weaker n-font-size-xs">Cmd+K</div>
        </nord-dropdown-item>
        <nord-dropdown-item>Help & Support</nord-dropdown-item>
        <nord-dropdown-item>API</nord-dropdown-item>
      </nord-dropdown-group>
      <nord-dropdown-item>
        Sign out
        <nord-icon slot="end" name="interface-logout" size="s"></nord-icon>
      </nord-dropdown-item>
    </nord-dropdown>
  </nord-navigation>
</template>
