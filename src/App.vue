<template>
<!-- Don't drop "q-app" class -->
<div id="q-app">
  <q-layout
    ref="layout"
    view="hHh Lpr fFf"
    :left-class="{'bg-grey-1': true}"
  >
    <q-toolbar v-ripple slot="header" flat color="primary">
      <q-btn flat @click="$refs.layout.toggleLeft()">
        <q-icon name="menu" />
      </q-btn>

      <q-toolbar-title>
        Menu
        <div slot="subtitle">{{$route.name}}</div>
      </q-toolbar-title>
       <div slot="right">Trial Φ Protocol</div>
    </q-toolbar>


    <!--   <q-tabs slot="navigation">
        <q-toolbar slot="title" icon="input" item to"/flows" hide="icon" label="Flows" />
      </q-tabs> -->

    <div slot="left">
      <!--
          Use <q-side-link> component
          instead of <q-item> for
          internal vue-router navigation
        -->

      <q-list no-border link inset-delimiter dense>
        <!-- <q-scroll-area slot="left" style="width: 100%; height: 100%"> -->
        <q-list-header>Menu</q-list-header>
        <q-side-link item to="/" exact>
          <q-item-side icon="home" />
          <q-item-main label="Home" sublabel="Main dashboard screen" />
        </q-side-link>
        <q-side-link item to="/charts">
          <q-item-side icon="insert chart" />
          <q-item-main label="Metrics" sublabel="Overview of important data" />
        </q-side-link>
        <q-side-link item to="/flows" exact>
          <q-item-side icon="link" />
          <q-item-main label="Audit Trail" sublabel="Blockchain-based audit logs" />
        </q-side-link>
        <q-side-link item to="/about" exact>
          <q-item-side icon="info" />
          <q-item-main label="About" sublabel="Trial Φ App Information" />
        </q-side-link>
        <q-list-header>Study Management</q-list-header>
        <q-side-link item to="/dashboard" exact>
          <q-item-side icon="view list" />
          <q-item-main label="Studies" sublabel="View all active studies" />
        </q-side-link>
        <q-side-link item to="null1" exact>
          <q-item-side icon="mode edit" />
          <q-item-main label="Manage" sublabel="Edit active studies" />
        </q-side-link>
        <q-side-link item to="null2" exact>
          <q-item-side icon="warning" />
          <q-item-main label="Queries" sublabel="View and resolve queries" />
        </q-side-link>
        <q-list-header>Subject Management</q-list-header>
        <q-side-link item to="null3" exact>
          <q-item-side icon="group" />
          <q-item-main label="Subjects" sublabel="View study participants" />
        </q-side-link>
        <q-side-link item to="null4" exact>
          <q-item-side icon="search" />
          <q-item-main label="Search" sublabel="Find study participants" />
        </q-side-link>
        <q-side-link item to="null5" exact>
          <q-item-side icon="date range" />
          <q-item-main label="Visits" sublabel="Subject visit calendar" />
        </q-side-link>
        <q-side-link item to="null6">
          <q-item-side icon="group add" />
          <q-item-main label="Manage" sublabel="Edit study participants" />
        </q-side-link>
        <q-list-header>Document Management</q-list-header>
        <q-side-link item to="null7" exact>
          <q-item-side icon="find in page" />
          <q-item-main label="Find" sublabel="Find a document" />
        </q-side-link>
        <q-side-link item to="null8" exact>
          <q-item-side icon="note add" />
          <q-item-main label="Create" sublabel="Create a new document" />
        </q-side-link>
        <q-side-link item to="null9" exact>
          <q-item-side icon="insert drive file" />
          <q-item-main label="Templates" sublabel="Manage document templates" />
        </q-side-link>
          <q-item-separator />
        <q-list-header>Settings</q-list-header>
        <q-side-link item to="/admin" exact>
          <q-item-side icon="settings" />
          <q-item-main label="Settings" sublabel="General settings" />
        </q-side-link>
        <q-side-link item to="null10" exact>
          <q-item-side icon="person" />
          <q-item-main label="Users" sublabel="Manage users" />
        </q-side-link>
        <q-side-link item to="null11" exact>
          <q-item-side icon="lock" />
          <q-item-main label="Access Controls" sublabel="Manage access levels" />
        </q-side-link>
     <!-- </q-scroll-area> -->
      </q-list>
    </div>

      <router-view />

    <q-toolbar slot="footer" color="primary">
    <q-toolbar-title />
    <div slot="right">Trial Φ Protocol</div>
  </q-toolbar>
  </q-layout>
</div>
</template>

<script>
/*
 * Root component
 */
import {
  QLayout,
  QToolbar,
  QToolbarTitle,
  QBtn,
  QIcon,
  QList,
  QListHeader,
  QItem,
  QItemSide,
  QItemMain,
  QSideLink,
  Ripple,
} from 'quasar';

export default {
  name: 'index',
  directives: {
    Ripple,
  },
  components: {
    QLayout,
    QToolbar,
    QToolbarTitle,
    QBtn,
    QIcon,
    QList,
    QListHeader,
    QItem,
    QItemSide,
    QItemMain,
    QSideLink,
  },
};
</script>

<style>

</style>
