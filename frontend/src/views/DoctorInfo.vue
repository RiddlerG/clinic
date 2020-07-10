<template>
  <div>
    <v-sheet
        color="#50a6c9"
        class="py-8"
        dark
    >
      <v-container>
        <v-row>
          <v-col cols="8" offset="2">
            <h1 class="font-weight-regular">Иванов Иван Иванович</h1>
            <v-breadcrumbs
              large
              :items="items"
              class="pa-0"
              dark
            >
              <template v-slot:item="{ item }">
                <v-breadcrumbs-item
                  :href="item.href"
                  :disabled="item.disabled"
                  class="font-weight-light red--text"
                >
                  {{ item.text }}
                </v-breadcrumbs-item>
              </template>
            </v-breadcrumbs>
          </v-col>
        </v-row>
      </v-container>
    </v-sheet>

    <v-container
      class="py-10"
    >
      <v-row>
        <v-col offset="2" cols="5">
          <v-img
            src="https://ld-wp73.template-help.com/beclinic/default/wp-content/uploads/2019/10/team-2-770x460.jpg"
            width="100%"
          ></v-img>
        </v-col>
        <v-col cols="3" class="pl-5">
          <v-card
            dark
            tile
            color="#24466f"
            class="pa-5"
          >
            <v-card-title class="p">
              <h3 class="font-weight-regular">Краткая информация</h3>
            </v-card-title>

            <v-list color="#24466f">
              <v-list-item>
                <v-list-item-subtitle>Фамилия:</v-list-item-subtitle>
                <v-list-item-title class="text-right">Иванов</v-list-item-title>
              </v-list-item>
              <v-divider :inset="inset"></v-divider>
              <v-list-item>
                <v-list-item-subtitle>Имя:</v-list-item-subtitle>
                <v-list-item-title class="text-right">Иван</v-list-item-title>
              </v-list-item>
              <v-divider :inset="inset"></v-divider>
              <v-list-item>
                <v-list-item-subtitle>Отчество:</v-list-item-subtitle>
                <v-list-item-title class="text-right">Иванович</v-list-item-title>
              </v-list-item>
              <v-list-item>
                <v-list-item-subtitle>Телефон:</v-list-item-subtitle>
                <v-list-item-title class="text-right">+7 (967) 451 - 33 - 21</v-list-item-title>
              </v-list-item>
              <v-list-item>
                <v-list-item-subtitle>Специальность:</v-list-item-subtitle>
                <v-list-item-title class="text-right">Терапевт</v-list-item-title>
              </v-list-item>
            </v-list>

            <v-card-actions class="py-10">
              <v-spacer></v-spacer>
              <v-btn
                color="#ffffff"
                light
                depressed
                tile
                class="pa-7"
              >
                Записаться на приём
              </v-btn>
              <v-spacer></v-spacer>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          text: 'Главная',
          disabled: false,
          href: 'breadcrumbs_dashboard',
        },
        {
          text: 'Врачи',
          disabled: false,
          href: 'breadcrumbs_link_1',
        },
        {
          text: 'Иванов Иван Иванович',
          disabled: true,
          href: 'breadcrumbs_link_1',
        },
      ],
    }),
  }
</script>