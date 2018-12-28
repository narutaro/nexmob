<template>
  <v-ons-page>

  <div class="toolbar toolbar--material">
    <div class="toolbar__left toolbar--material__left">
    </div>

    <div class="toolbar__center toolbar--material__center app-css-title-center">
      <span>Datacenters</span>
    </div>

    <div class="toolbar__right toolbar--material__right">
    </div>
  </div>


  <ul class="list list--material">
    <li class="list-item list-item--material" v-for="dc in datacenters">

      <div class="list-item__left list-item--material__left">
        <img class="list-item__thumbnail list-item--material__thumbnail" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACgAAAAoCAIAAAADnC86AAAACXBIWXMAAAsTAAALEwEAmpwYAAAAB3RJTUUH3wwJCB8v/9zErgAAABl0RVh0Q29tbWVudABDcmVhdGVkIHdpdGggR0lNUFeBDhcAAAAvSURBVFjD7c0BDQAACAMgtX+KJzWGm4MCdJK6MHVELBaLxWKxWCwWi8VisVj8MV7qBgI2A8rYpgAAAABJRU5ErkJggg==">
      </div>

      <div @click="selectedDC(dc.id)" class="list-item__center list-item--material__center list-item--chevron list-item--tappable">
        <div class="list-item__title list-item--material__title">{{ dc.name }}</div>
        <div class="list-item__subtitle list-item--material__subtitle"><ons-icon icon="fa-map-marker-alt"></ons-icon> {{ dc.timezone }}</div>
      </div>

    </li>
  </ul>

  <div class="tabbar">
    <label class="tabbar__item">
      <!-- <input type="radio" name="tabbar-b"> -->
      <button @click="users" class="tabbar__button">
        <ons-icon icon="fa-users" fixed-width="false" size="2x"></ons-icon>
      </button>
    </label>

    <label class="tabbar__item">
      <input type="radio" name="tabbar-b">
      <button class="tabbar__button">
        <i class="tabbar__icon ion-record"></i>
      </button>
    </label>

    <label class="tabbar__item">
      <input type="radio" name="tabbar-b">
      <button class="tabbar__button">
      <!-- <i class="tabbar__icon ion-star"></i> -->
        <ons-icon @click="logout" icon="fa-sign-out-alt" fixed-width="false" size="2x"></ons-icon>
      </button>
    </label>
  </div>

  </v-ons-page>
</template>

