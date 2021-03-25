<template>
  <div>
    <div class="latest-journals-heading container" data-v-460714ac="">
      <span class="label" data-v-460714ac=""> Latest and greatest </span>
    </div>
    <div class="latest-journals" data-v-460714ac="">
      <div class="container" data-v-460714ac="">
        <template v-for="edge in $page.list.edges">
          <g-link to="/Journal/" class="journal" data-v-460714ac="" v-if="edge.node.listDisplay" :key="edge.node.id">
            <h3 class="journal-title" data-v-460714ac="">
              {{ edge.node.title }}
            </h3>
          </g-link>
        </template>
        <!-- <a href="./Journal" class="journal" data-v-460714ac="">
          <h3 class="journal-title" data-v-460714ac="">
            VueJS for your next project
          </h3>
        </a>
        <a href="./Journal" class="journal" data-v-460714ac="">
          <h3 class="journal-title" data-v-460714ac="">
            macOS development environment
          </h3>
        </a>
        <a href="./Journal" class="journal" data-v-460714ac="">
          <h3 class="journal-title" data-v-460714ac="">About Typography</h3>
        </a> -->
      </div>
    </div>
  </div>
</template>

<page-query>
	query{
		list: allStrapiPost{
			edges{
				node{
					id
					title
					listDisplay
					author

				}
			}
		}
	}
</page-query>
