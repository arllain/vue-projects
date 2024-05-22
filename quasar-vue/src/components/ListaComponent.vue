<!-- <template>
  <div class="q-pa-md">
    <q-table title="Treats" :rows="rows" :columns="columns" row-key="name" />
  </div>
</template>

<script>
const columns = [
  {
    name: 'name',
    required: true,
    label: 'Dessert (100g serving)',
    align: 'left',
    field: (row) => row.name,
    format: (val) => `${val}`,
    sortable: true,
  },
  {
    name: 'calories',
    align: 'center',
    label: 'Calories',
    field: 'calories',
    sortable: true,
  },
  { name: 'fat', label: 'Fat (g)', field: 'fat', sortable: true },
  { name: 'carbs', label: 'Carbs (g)', field: 'carbs' },
  { name: 'protein', label: 'Protein (g)', field: 'protein' },
  { name: 'sodium', label: 'Sodium (mg)', field: 'sodium' },
  {
    name: 'calcium',
    label: 'Calcium (%)',
    field: 'calcium',
    sortable: true,
    sort: (a, b) => parseInt(a, 10) - parseInt(b, 10),
  },
  {
    name: 'iron',
    label: 'Iron (%)',
    field: 'iron',
    sortable: true,
    sort: (a, b) => parseInt(a, 10) - parseInt(b, 10),
  },
  {
    name: 'acao',
    label: 'Ação',
    field: 'acao',
  },
];

const rows = [
  {
    name: 'Frozen Yogurt',
    calories: 159,
    fat: 6.0,
    carbs: 24,
    protein: 4.0,
    sodium: 87,
    calcium: '14%',
    iron: '1%',
    acao: 'ação',
  },
  {
    name: 'Ice cream sandwich',
    calories: 237,
    fat: 9.0,
    carbs: 37,
    protein: 4.3,
    sodium: 129,
    calcium: '8%',
    iron: '1%',
    acao: 'ação',
  },
  {
    name: 'Eclair',
    calories: 262,
    fat: 16.0,
    carbs: 23,
    protein: 6.0,
    sodium: 337,
    calcium: '6%',
    iron: '7%',
    acao: 'ação',
  },
  {
    name: 'Cupcake',
    calories: 305,
    fat: 3.7,
    carbs: 67,
    protein: 4.3,
    sodium: 413,
    calcium: '3%',
    iron: '8%',
    acao: 'ação',
  },
  {
    name: 'Gingerbread',
    calories: 356,
    fat: 16.0,
    carbs: 49,
    protein: 3.9,
    sodium: 327,
    calcium: '7%',
    iron: '16%',
    acao: 'ação',
  },
  {
    name: 'Jelly bean',
    calories: 375,
    fat: 0.0,
    carbs: 94,
    protein: 0.0,
    sodium: 50,
    calcium: '0%',
    iron: '0%',
  },
  {
    name: 'Lollipop',
    calories: 392,
    fat: 0.2,
    carbs: 98,
    protein: 0,
    sodium: 38,
    calcium: '0%',
    iron: '2%',
    acao: 'ação',
  },
  {
    name: 'Honeycomb',
    calories: 408,
    fat: 3.2,
    carbs: 87,
    protein: 6.5,
    sodium: 562,
    calcium: '0%',
    iron: '45%',
    acao: 'ação',
  },
  {
    name: 'Donut',
    calories: 452,
    fat: 25.0,
    carbs: 51,
    protein: 4.9,
    sodium: 326,
    calcium: '2%',
    iron: '22%',
    acao: 'ação',
  },
  {
    name: 'KitKat',
    calories: 518,
    fat: 26.0,
    carbs: 65,
    protein: 7,
    sodium: 54,
    calcium: '12%',
    iron: '6%',
    acao: 'ação',
  },
];

export default {
  setup() {
    return {
      columns,
      rows,
    };
  },
};
</script> -->

<!-- <template>
  <div>
    <q-h1>Teste</q-h1>
  </div>
</template> -->

<template>
  <!-- <q-page class="flex flex-center">
    <q-btn
      label="Open Example in a New Tab"
      color="primary"
      href="https://www.example.com"
      target="_blank"
      rel="noopener noreferrer"
    />
  </q-page> -->
  <div>
    <div class="q-pa-md">
      <q-btn class="glossy" round color="deep-orange" icon="local_activity">
        <q-menu context-menu anchor="center right" self="top right">
          <q-list dense style="min-width: 100px">
            <q-item clickable @click="openInNewTab('https://www.example.com')">
              <q-item-section> Abrir link em nova guia </q-item-section>
            </q-item>
            <q-separator />
            <q-item
              clickable
              @click="openInNewWindow('https://www.example.com')"
            >
              <q-item-section>Abrir link em nova janela</q-item-section>
            </q-item>
            <q-separator />
            <q-item
              clickable
              @click="notifyIncognitoOpen('https://www.example.com')"
            >
              <q-item-section>Abrir link em nova janela anônima</q-item-section>
            </q-item>
          </q-list>
        </q-menu>
      </q-btn>
    </div>
    <div class="q-pa-md">
      <q-btn class="glossy" round color="deep-orange" icon="local_activity">
        <q-menu context-menu anchor="center right" self="top right">
          <q-list dense style="min-width: 100px">
            <q-item clickable v-close-popup>
              <q-item-section>Abrir link em nova guia</q-item-section>
            </q-item>
            <q-separator />
            <q-item clickable v-close-popup>
              <q-item-section>Abrir link em nova janela</q-item-section>
            </q-item>
            <q-separator />
            <q-item clickable v-close-popup>
              <q-item-section>Abrir link em nova janela anônima</q-item-section>
            </q-item>
          </q-list>
        </q-menu>
      </q-btn>
    </div>
    <div class="q-pa-md">
      <q-btn class="glossy" round color="deep-orange" icon="local_activity">
        <q-menu context-menu anchor="center right" self="top right">
          <q-list dense style="min-width: 100px">
            <q-item clickable v-close-popup>
              <q-item-section>Abrir link em nova guia</q-item-section>
            </q-item>
            <q-separator />
            <q-item clickable v-close-popup>
              <q-item-section>Abrir link em nova janela</q-item-section>
            </q-item>
            <q-separator />
            <q-item clickable v-close-popup>
              <q-item-section>Abrir link em nova janela anônima</q-item-section>
            </q-item>
          </q-list>
        </q-menu>
      </q-btn>
    </div>
    <div class="q-pa-md">
      <q-btn class="glossy" round color="deep-orange" icon="local_activity">
        <q-menu context-menu anchor="center right" self="top right">
          <q-list dense style="min-width: 100px">
            <q-item clickable v-close-popup>
              <q-item-section>Abrir link em nova guia</q-item-section>
            </q-item>
            <q-separator />
            <q-item clickable v-close-popup>
              <q-item-section>Abrir link em nova janela</q-item-section>
            </q-item>
            <q-separator />
            <q-item clickable v-close-popup>
              <q-item-section>Abrir link em nova janela anônima</q-item-section>
            </q-item>
          </q-list>
        </q-menu>
      </q-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  methods: {
    openInNewTab(url) {
      window.open(url, '_blank', 'noopener,noreferrer');
    },

    openInNewWindow(url) {
      window.open(url, '_blank', 'noopener,noreferrer,width=800,height=600');
    },

    notifyIncognitoOpen(url) {
      // Inform the user how to open the link in incognito mode
      this.$q.notify({
        message: `To open this link in an incognito window, please manually open a new incognito window in your browser and paste the following URL: ${url}`,
        color: 'primary',
        timeout: 6000,
        actions: [
          {
            label: 'Copy URL',
            color: 'white',
            handler: () => this.copyToClipboard(url),
          },
        ],
      });
    },
  },
};
</script>

<style scoped>
.btn-actions .q-btn {
  padding: 10px;
}
</style>
