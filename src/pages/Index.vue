<template>

  <Layout>

   
     <div class="container">
			<div class="hero">
				<h1 class="hero-title">Simplicity. Aesthetics. Value.</h1>
				<h2 class="hero-subtitle">
					Hi there, I'm an independent Digital Designer &amp; Art Director focused on digital design for brands that like to
					have fun.
				</h2>
			</div>
			
			<div class="projects" data-v-50cbff3e="">
				<template v-for="edge in $page.list.edges">
					<div class="project" data-v-50cbff3e=""  v-if="!edge.node.listDisplay" :key="edge.node.id">
						<g-link :to="'/post/' + edge.node.id" class="project-link" data-v-50cbff3e="">
							<img :src="edge.node.urls" class="thumbnail g-image g-image--lazy g-image--loading" width="2560">
							<h3 class="project-title" data-v-50cbff3e="">{{ edge.node.title }}</h3>
							<div class="categories" data-v-50cbff3e="">
								<span class="category" data-v-50cbff3e="">{{ edge.node.author }}</span>
								<span class="category" data-v-50cbff3e="">pink</span>
							</div>
						</g-link>
					</div>
				</template>
				<!-- <div class="project" data-v-50cbff3e="">
					<a href="./Details" class="project-link" data-v-50cbff3e="">
						<img src="/img/a1.jpg" class="thumbnail g-image g-image--lazy g-image--loading" width="2560">
						<h3 class="project-title" data-v-50cbff3e="">Banana</h3>
						<div class="categories" data-v-50cbff3e="">
							<span class="category" data-v-50cbff3e="">photography</span>
							<span class="category" data-v-50cbff3e="">pink</span>
						</div>
					</a>
				</div>
				<div class="project" data-v-50cbff3e="">
					<a href="./Details" class="project-link" data-v-50cbff3e="">
						<img src="/img/a2.jpg" class="thumbnail g-image g-image--lazy g-image--loading" width="2560">
						<h3 class="project-title" data-v-50cbff3e="">Pineapple</h3>
						<div class="categories" data-v-50cbff3e="">
							<span class="category" data-v-50cbff3e="">photography</span>
							<span class="category" data-v-50cbff3e="">blue</span>
						</div>
					</a>
				</div>
				<div class="project" data-v-50cbff3e="">
					<a href="./Details" class="project-link" data-v-50cbff3e="">
						<img src="/img/a3.jpg" class="thumbnail g-image g-image--lazy g-image--loading" width="2560">
						<h3 class="project-title" data-v-50cbff3e="">Ice Cream</h3>
						<div class="categories" data-v-50cbff3e="">
							<span class="category" data-v-50cbff3e="">photography</span>
							<span class="category" data-v-50cbff3e="">yellow</span>
						</div>
					</a>
				</div>
				<div class="project" data-v-50cbff3e="">
					<a href="./Details" class="project-link" data-v-50cbff3e="">
						<img src="/img/a4.jpg" class="thumbnail g-image g-image--lazy g-image--loading" width="2560">
						<h3 class="project-title" data-v-50cbff3e="">Porta400</h3>
						<div class="categories" data-v-50cbff3e="">
							<span class="category" data-v-50cbff3e="">photography</span>
							<span class="category" data-v-50cbff3e="">yellow</span></div>
					</a>
				</div> -->
			</div>
		</div> 

    <navs />

  </Layout>
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
					pic{
						url
					}
					urls
				}
			}
		}
	}
</page-query>

<script>
import navs from './nav.vue'
export default {
  metaInfo: {
    title: 'HomePage'
  },
  components: {
        navs
  },
  data () {
    return {
		lost: 'http://117.50.64.225:1337'
	}
  }	
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
