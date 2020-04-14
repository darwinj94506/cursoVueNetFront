<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      :clipped="$vuetify.breakpoint.lgAndUp"
      app
    >
      <v-list dense>
        <template >
          <v-list-group append-icon="">
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>
                  Almacén
                </v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  <router-link :to="{ path:'categorias' }">
                    Categorías
                  </router-link>
                  
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Artículos
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </template>

        <template >
          <v-list-group append-icon="">
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>
                  Compras
                </v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Ingreso 
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
             <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Proveedores
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </template>

        <template >
          <v-list-group append-icon="">
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>
                  Ventas
                </v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Ventas
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
              <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Clientes
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </template>
        <template >
          <v-list-group append-icon="">
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>
                  Accesos
                </v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Roles
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
             <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Usuarios
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </template>
        <template >
          <v-list-group append-icon="">
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>
                  Consultas
                </v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Consultas Compras
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
             <v-list-item link>
              <v-list-item-action>
                <v-icon>home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Consultas Ventas
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </template>
      </v-list>



    </v-navigation-drawer>

    <v-app-bar
      :clipped-left="$vuetify.breakpoint.lgAndUp"
      app
      color="blue darken-3"
      dark
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title
        style="width: 300px"
        class="ml-0 pl-4"
      >
        <span class="hidden-sm-and-down">Google Contacts</span>
      </v-toolbar-title>
      <v-text-field
        flat
        solo-inverted
        hide-details
        prepend-inner-icon="mdi-magnify"
        label="Search"
        class="hidden-sm-and-down"
      />
      <v-spacer />
      <v-btn icon>
        <v-icon>mdi-apps</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-bell</v-icon>
      </v-btn>
      <v-btn
        icon
        large
      >
        <v-avatar
          size="32px"
          item
        >
          <v-img
            src="https://cdn.vuetifyjs.com/images/logos/logo.svg"
            alt="Vuetify"
          /></v-avatar>
      </v-btn>
    </v-app-bar>

    <v-content>
      <v-container fluid fill-height>
        <v-slide-y-transition mode="out-in">
          <router-view></router-view> 
        </v-slide-y-transition>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
  export default {
    props: {
      source: String,
    },
    data: () => ({
      dialog: false,
      drawer: null,
      items: [
       
        {
          icon: 'md-chevron-up',
          'icon-alt': 'md-chevron-down',
          text: 'Almacén',
          model: true,
          children: [
            { icon: 'md-home', text: 'Categorías' },
            { icon: 'home', text: 'Artículos' }
            
          ],
        },
        {
          icon: 'md_home',
          'icon-alt': 'md-chevron-down',
          text: 'More',
          model: false,
          children: [
            { text: 'Import' },
            { text: 'Export' },
            { text: 'Print' },
            { text: 'Undo changes' },
            { text: 'Other contacts' },
          ],
        },
        { icon: 'mdi-settings', text: 'Settings' },
        { icon: 'md-message', text: 'Send feedback' },
        { icon: 'md-help-circle', text: 'Help' },
        { icon: 'md-cellphone-link', text: 'App downloads' },
        { icon: 'md-keyboard', text: 'Go to the old version' },
      ],
    }),
  }
</script>