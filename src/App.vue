<template>
  <div id="app">
    <div class="page-container">
      <md-app>
        <md-app-toolbar class="md-primary" md-elevation="0">
          <md-button class="md-icon-button" @click="toggleMenu" v-if="!menuVisible">
            <md-icon>menu</md-icon>
          </md-button>
          <span class="md-title">NoKo Dashboard</span>
        </md-app-toolbar>

        <md-app-drawer :md-active.sync="menuVisible" md-persistent="mini">
          <md-toolbar class="md-transparent" md-elevation="0">
            <span>Navigation</span>
            <div class="md-toolbar-section-end">
              <md-button class="md-icon-button md-dense" @click="toggleMenu">
                <md-icon>keyboard_arrow_left</md-icon>
              </md-button>
            </div>
          </md-toolbar>

          <md-list>
            <md-list-item to="/" exact>
              <md-icon>move_to_inbox</md-icon>
              <span class="md-list-item-text">Inbox</span>
            </md-list-item>

            <md-list-item to="/category">
              <md-icon>send</md-icon>
              <span class="md-list-item-text">Send Email</span>
            </md-list-item>

            <md-list-item>
              <md-icon>delete</md-icon>
              <span class="md-list-item-text">Trash</span>
            </md-list-item>

            <md-list-item>
              <md-icon>error</md-icon>
              <span class="md-list-item-text">Spam</span>
            </md-list-item>
          </md-list>
        </md-app-drawer>

        <md-app-content>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus alias dolorum ea et labore minima nihil pariatur quas rem tenetur! Architecto consequatur dolores dolorum perspiciatis. Atque cumque error nam neque.
        </md-app-content>
      </md-app>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    menuVisible: false
  }),
  methods: {
    toggleMenu(){
      this.menuVisible = !this.menuVisible
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto:300,400,500,700,400italic|Material+Icons');

.md-app{
  min-height: 100vh;
}
</style>
