<template>
  <v-treeview
    v-model="tree"
    :open="initiallyOpen"
    :items="items"
    activatable
    item-key="name"
    open-on-click
  >
    <template v-slot:prepend="{ item, open }">
      <v-icon v-if="item.children">
        {{ open ? 'mdi-folder-open' : 'mdi-folder' }}
      </v-icon>
      <Icon v-else :icon="item.logo" />
    </template>
  </v-treeview>
</template>

<script>
// @ is an alias to /src
import { Icon } from '@iconify/vue2';
export default {
  name: "Treeview",
  components: {
		Icon,
	},
    data: () => ({
      initiallyOpen: ['BE'],
      tree: [],
      items: [
        {
          name: 'DevOps',
          children: [
              {
                  name: 'AWS',
                  logo: 'logos:aws'
              },
              {
                  name: 'Nginx',
                  logo: 'logos:nginx',
              },
              {
                  name: 'Tomcat',
                  logo: 'logos:tomcat',
              },
              {
                  name: 'Docker',
                  logo: 'logos:docker-icon'
              },
              {
                  name: 'MariaDB',
                  logo : 'logos:mariadb-icon'
              },
              {
                  name: 'MYSQL',
                  logo : 'logos:mysql'
              },
          ]
        },
        {
          name: 'BE',
          children: [
              {
                  name: 'Java',
                  logo: 'logos:java',
              },
              {
                  name: 'Springboot',
                  logo: 'logos:spring-icon',
              },
              {
                  name: 'JPA',
                  logo: 'mdi-database'
              },
              {
                  name: 'MyBatis',
                  logo: 'mdi-database'
              },
          ]
        },
        {
          name: 'FE',
          children: [
            {
              name: 'Vue',
              logo: 'logos:vue',
            },
            {
              name: 'html',
              logo: 'logos:html-5',
            },
            {
              name: 'css',
              logo: 'logos:css-3',
            },
            {
              name: 'JavaScript',
              logo: 'logos:javascript',
            },
          ],
        },
        {
          name: 'Collaboration Tools',
          children : [
              {
                name: 'Git',
                logo: 'logos:git-icon',
              },
              {
                name: 'github',
                logo: 'logos:github-icon',
              },
              {
                name: 'Jira',
                logo: 'logos:jira'
              },
          ],
        },
      ],
    }),
  }

</script>